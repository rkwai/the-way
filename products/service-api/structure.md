# Service Structure Template

```
products/service-api/
├── src/
│   ├── main.ts            # Bootstrap the HTTP server / application entrypoint
│   ├── app.module.ts      # Dependency injection and module wiring
│   ├── controllers/       # Transport layer
│   ├── services/          # Business logic
│   ├── repositories/      # Data access
│   └── schemas/           # Validation or ORM models
├── tests/
│   ├── unit/
│   └── integration/
├── contracts/
│   ├── http/
│   └── events/
├── migrations/
└── package.json
```

Adapt this outline to your stack. The goal is to make it obvious where code lives and how to run it.
