# n8n Automation - Child Story Creation

This repository contains a sanitized n8n workflow template for generating a personalized children's storybook. The workflow receives a story idea through a webhook, uses AI to create a five-scene story, generates matching images, turns the scenes into an HTML/PDF storybook, uploads the result to Google Drive, and emails the PDF to the requested recipient.

The workflow file is safe for GitHub: credentials, hardcoded tokens, and personal account IDs have been removed.

## What The Project Offers

- A webhook-based story request flow.
- AI parsing for the child story inputs: character, setting, and theme.
- Five-scene story generation.
- Scene splitting and scene/image alignment.
- AI image generation for each scene.
- Optional image compression/resize flow.
- HTML storybook assembly.
- PDF generation through an external PDF conversion API.
- Google Drive upload.
- Email delivery with the generated PDF attached.

## Workflow File

```text
workflows/child-story-creation.workflow.json
```

Import this file into n8n, reconnect your credentials, test the webhook, and activate the workflow.

## Expected Webhook Payload

The workflow listens for:

```http
POST /generate-image
Content-Type: application/json
```

Example body:

```json
{
  "character": "Lina, a curious child who loves the sea",
  "setting": "a glowing underwater city",
  "theme": "courage, kindness, and teamwork",
  "email": "parent@example.com"
}
```

A reusable example is available in [examples/sample-request.json](examples/sample-request.json).

## High-Level Flow

```text
Webhook
  -> Set request fields
  -> Parse story inputs with OpenAI
  -> Generate five story scenes with OpenAI
  -> Split scenes into items
  -> Generate or fetch scene images
  -> Compress/extract image binary
  -> Align scenes with images
  -> Build HTML storybook
  -> Convert HTML to PDF
  -> Email PDF to recipient
  -> Upload/store file in Google Drive
```

## Required Services

- n8n
- OpenAI API credential
- Hugging Face API token for FLUX image generation
- PDFShift API credential for PDF conversion
- SMTP credential for email delivery
- Google Drive OAuth credential
- Optional Tinify/Image compression credential

Setup details are in [docs/IMPORT_AND_SETUP.md](docs/IMPORT_AND_SETUP.md).

## Repository Structure

```text
.
├── workflows/
│   └── child-story-creation.workflow.json
├── examples/
│   └── sample-request.json
├── docs/
│   ├── IMPORT_AND_SETUP.md
│   ├── WORKFLOW_OVERVIEW.md
│   ├── SECURITY.md
│   └── GITHUB_DESCRIPTION.md
├── .env.example
├── .gitignore
└── README.md
```

## Recommended GitHub Description

```text
n8n workflow automation that generates personalized AI children's storybooks with story scenes, images, PDF conversion, Google Drive storage, and email delivery.
```

Suggested topics:

```text
n8n, automation, workflow, openai, ai-story-generation, children-story, pdf-generation, google-drive, email-automation, no-code
```

## Security Notice

Do not commit exported n8n credentials or real API tokens. This repository contains a sanitized workflow template only. Reconnect credentials inside your own n8n instance after import.
