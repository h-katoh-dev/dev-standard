# Repository Structure

```text
.
├── AI_RULES.md
├── README.md
├── docs/
│   ├── architecture.md
│   ├── contribution.md
│   ├── philosophy.md
│   └── repository-structure.md
├── catalog/
│   ├── features.md
│   └── patterns.md
├── standards/
│   ├── security/
│   ├── api/
│   ├── database/
│   ├── ui/
│   └── testing/
├── patterns/
│   ├── authentication/
│   ├── authorization/
│   ├── user/
│   ├── form/
│   └── notification/
├── templates/
│   ├── web/
│   ├── api/
│   └── app/
├── variants/
│   └── README.md
└── schemas/
    ├── feature.schema.json
    ├── pattern.schema.json
    └── selection.schema.json
```

## Rules

- Empty directories are not meaningful in Git, so placeholder files may be used until content exists.
- Do not create technology-specific directories at the conceptual layer unless the technology boundary is explicit.
- Prefer small, composable artifacts over monolithic templates.
- A Template must declare the Standard/Pattern it implements.
- A Variant must explain why it differs from the Standard and whether it is a candidate for promotion.
- Public repository safety rules in `AI_RULES.md` override convenience.
