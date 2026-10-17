# flowguard-tests

Suites de pruebas de FlowGuard: unitarias (Vitest), de integración, de contrato y end-to-end (Playwright).

**Responsabilidad:** cada propietario mantiene las pruebas funcionales de su módulo (Dev 1: backend; Dev 2: interfaz y E2E de usuario; Dev 3: agente y proveedor). **Dev 5** coordina la suite compartida (pruebas de contrato y compatibilidad transversal) y registra los defectos transversales. **Dev 4** configura la CI que las ejecuta, sin ser responsable funcional de las pruebas. Ver [flowguard-docs/testing.md § Responsables de las pruebas](https://github.com/FlowGuard-Hackathon/flowguard-docs/blob/main/testing.md#responsables-de-las-pruebas).

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

Este repo todavía no tiene pruebas; está preparado para que Dev 5 (coordinación) y los propietarios de cada módulo empiecen siguiendo el Bloque 1 de [flowguard-docs/implementation-checklist.md](https://github.com/FlowGuard-Hackathon/flowguard-docs/blob/main/implementation-checklist.md).
