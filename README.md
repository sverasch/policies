# Policies

Source of truth for privacy policies and support pages published under
`citadelofricks.ai`. One directory per product; HTML files are self-contained
(no external CSS/JS/fonts) and are deployed by copying them into the static
site repo (`citadelofricks.ai/public/<path>/index.html`, served by Cloudflare
Pages).

## Layout

```
vllm-monitor/
├── privacy.html    # → citadelofricks.ai/privacy/vllmmonitor
└── support.html    # → citadelofricks.ai/support/vllmmonitor
TEMPLATE.html       # copy for new products
```

## Rules

- **No absolute domain references inside pages.** Relative links and the
  contact email only — pages must survive a domain move untouched.
- Keep the privacy wording in sync with each app's App Store privacy nutrition
  label ("Data Not Collected" here) — a mismatch is a review reject magnet.
- Update the visible "Last updated" date on every change.
- Contact address: `vllmmonitor@citadelofricks.ai` (Google Workspace alias).

## Products ↔ consumers

| Product | Pages | In-app constants |
|---|---|---|
| vLLM Monitor | `/privacy/vllmmonitor`, `/support/vllmmonitor` | `AppInfo.swift` in `sverasch/vllm-monitor` |
