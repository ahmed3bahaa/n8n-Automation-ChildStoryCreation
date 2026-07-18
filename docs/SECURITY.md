# Security Notes

This repository is designed to be safe for public GitHub use.

## What Was Removed

The committed workflow template does not include:

- Real bearer tokens.
- n8n credential IDs.
- n8n credential names tied to a private instance.
- Personal sender email values.
- Google Drive folder URLs from the source export.

## What To Avoid

Never commit:

- `credentials.json`
- n8n local database files
- `.env`
- API keys
- SMTP passwords
- OAuth tokens
- Real webhook secrets

## Recommended Credential Handling

Store secrets inside n8n credentials or environment variables:

```text
OPENAI_API_KEY
HUGGINGFACE_API_TOKEN
PDFSHIFT_API_KEY
TINIFY_API_KEY
SMTP_FROM_EMAIL
```

## Before Pushing Future Workflow Exports

Run a secret scan:

```bash
grep -R "Bearer\\|apiKey\\|password\\|secret\\|hf_" .
```

On PowerShell:

```powershell
Select-String -Path .\**\* -Pattern "Bearer|apiKey|password|secret|hf_" -CaseSensitive:$false
```

If a real token appears, remove it before committing.
