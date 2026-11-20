

<!-- local-development:start -->
# Desarrollo local

Puedes abrir este repositorio en VS Code, Antigravity o Sublime Text. El compilador y los servicios necesarios dependen del componente indicado abajo.

## Node.js

Usa los scripts y el archivo de bloqueo de cada componente; revisa `engines` antes de elegir Node. La máquina de revisión tiene Node 22.23.1, pero eso no certifica compatibilidad de las dependencias antiguas.

[click/package.json](<click/package.json>): `start`.

```powershell
Set-Location 'click'
npm.cmd ci
npm.cmd run
```

## Componentes y validación

Inventario y compilaciones locales del 2026-11-15. Una compilación correcta no acredita todavía interacción, compatibilidad de base de datos, instalador ni despliegue.

| Componente | Tipo / destino | Validación |
| --- | --- | --- |
| [click/package.json](<click/package.json>) | node | Sin ejecutar |

## Archivos ignorados

`.gitignore` excluye credenciales locales, estado del editor y salidas de las herramientas detectadas. No deja de versionar archivos que ya estaban en Git. Los manifiestos, archivos de bloqueo, recursos fuente y scripts de esquema forman parte del código.
<!-- local-development:end -->

<!-- improvements-20261119:start -->
## Mejoras y verificación funcional (2026-11-19)

- **Mejoras aplicadas:** Servidor HTTP nativo Node 22+ sin dependencias vulnerables (`click/server.mjs` y `click/lib/store.mjs`), corrección de `routes/sessions.js`, interfaz responsiva con los 4 contadores operativos (Cookies, Sessions, LocalStorage y API DB con `+1`/`−1`/`Reiniciar` y sincronización entre pestañas).
- **Pruebas ejecutadas:** `node --test click/tests/app.test.mjs` (prueba HTTP en vivo aprobada: HTML, `/health`, `/sessions`, `/cookies` y CRUD persistente `/api/v1/clicks`).
<!-- improvements-20261119:end -->
