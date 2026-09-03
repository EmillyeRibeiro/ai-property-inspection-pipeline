# Architecture

```text
Client / Inspection UI
        |
        v
Sequential Upload Webhook
        |
        v
Session Storage
        |
        v
Inspection Processing Webhook
        |
        +--> Gemini Files API
        |       |
        |       v
        |   Multimodal Analysis
        |       |
        |       v
        |   Structured Refinement
        |
        v
HTML Report -> Gotenberg -> PDF

Entry PDF + Exit PDF
        |
        v
Gemini Comparison
        |
        v
Comparison HTML -> PDF -> Optional CRM delivery
```

The workflow is split into independent stages so uploads, long-running multimodal processing, and report comparison can be operated separately.
