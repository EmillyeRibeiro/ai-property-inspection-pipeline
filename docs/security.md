# Security notes

The public workflows are sanitized. Before using them:

- Create your own n8n credentials for Gemini.
- Replace all `REPLACE_WITH_YOUR_N8N_CREDENTIAL_ID` placeholders.
- Configure your own inspection domain and storage paths.
- Configure Bitrix24 only if CRM delivery is required.
- Keep secrets in n8n Credentials or environment variables, never in Code nodes.
- Restrict webhook origins and add authentication appropriate to your deployment.
- Do not process real tenant/owner data in a public demo environment.
