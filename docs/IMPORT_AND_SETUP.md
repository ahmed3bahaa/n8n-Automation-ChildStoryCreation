# Import And Setup Guide

This guide explains how to import and configure the workflow in n8n.

## 1. Import The Workflow

1. Open your n8n instance.
2. Go to **Workflows**.
3. Choose **Import from File**.
4. Select:

```text
workflows/child-story-creation.workflow.json
```

5. Save the imported workflow.

## 2. Reconnect Credentials

The GitHub version is sanitized, so you must reconnect credentials inside n8n.

Required credentials:

| Service | Used By Nodes | Purpose |
| --- | --- | --- |
| OpenAI | `Parser`, `Split`, `Generate-image` | Parse input, write scenes, optionally generate images |
| Hugging Face API | `flux.ai` | Generate FLUX scene images |
| PDFShift | `pdf.call` | Convert HTML storybook into PDF |
| SMTP | `Send Email` | Send the finished storybook |
| Google Drive OAuth | `Google Drive`, `Google Drive1` | Upload or organize generated files |
| Tinify/basic auth, optional | `compress-image1`, `compress` | Compress generated images |

## 3. Environment Variables

Use `.env.example` as a reminder for the values needed by your n8n environment:

```text
OPENAI_API_KEY
HUGGINGFACE_API_TOKEN
PDFSHIFT_API_KEY
TINIFY_API_KEY
SMTP_FROM_EMAIL
```

The sanitized workflow uses this expression for the Hugging Face authorization header:

```text
=Bearer {{$env.HUGGINGFACE_API_TOKEN}}
```

The email sender is also environment-based:

```text
={{$env.SMTP_FROM_EMAIL}}
```

## 4. Test The Webhook

Send a POST request to your n8n webhook URL:

```bash
curl -X POST "https://your-n8n-domain/webhook/generate-image" \
  -H "Content-Type: application/json" \
  -d @examples/sample-request.json
```

For local n8n test mode, use the test webhook URL shown by the Webhook node.

## 5. Activate

After confirming the workflow runs successfully:

1. Save the workflow.
2. Activate it.
3. Use the production webhook URL.

## 6. Common Setup Issues

- If OpenAI nodes fail, confirm the OpenAI credential is selected on all OpenAI nodes.
- If image generation fails, confirm the Hugging Face token is available to n8n.
- If PDF conversion fails, reconnect PDFShift credentials.
- If email delivery fails, verify SMTP host, port, username, password, sender email, and attachment field.
- If Google Drive upload fails, reconnect OAuth and choose the correct destination folder.
