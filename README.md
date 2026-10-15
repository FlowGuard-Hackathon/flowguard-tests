# flowguard-tests

Suites de pruebas de FlowGuard: unitarias (Vitest), de integración, de contrato y end-to-end (Playwright).

**Responsable principal:** Dev 4 (contratos compartidos, mocks, pruebas, documentación, QA), con casos aportados por cada developer para su propio módulo.

## Alcance

Según [flowguard-docs/architecture.md § 3](https://github.com/FlowGuard-Hackathon/flowguard-docs/blob/main/architecture.md#3-estructura-del-repositorio):

```
tests/
├── unit/
├── integration/
├── contract/
├── e2e/
└── fixtures/
```

El plan de pruebas completo — qué cubre cada suite, los 15 escenarios obligatorios del mecanismo asíncrono, idempotencia, rate limiting y RLS — está especificado en [flowguard-docs/testing.md](https://github.com/FlowGuard-Hackathon/flowguard-docs/blob/main/testing.md). Ese documento distingue qué se ha verificado realmente (contra PostgreSQL real, ver la nota en flowguard-docs/database.md) de lo que solo queda especificado para implementarse aquí.

## Dependencias de otros repos

- `flowguard-mocks`: fixtures usados por las pruebas de contrato y E2E.
- `flowguard-src` y `flowguard-app`: el código bajo prueba.
- `flowguard-supabase`: el esquema contra el que corren las pruebas de integración (recomendado: un proyecto Supabase de pruebas o un PostgreSQL local/Docker, nunca el de producción).

Este repo todavía no tiene pruebas; está preparado para que Dev 4 empiece siguiendo el Bloque 1 de [flowguard-docs/implementation-checklist.md](https://github.com/FlowGuard-Hackathon/flowguard-docs/blob/main/implementation-checklist.md).
