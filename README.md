# Cosmic-Workspace

Archivos de la raíz del árbol de CosmicOS: el workspace de Cargo y la configuración de Rust.

| Archivo | Para qué sirve |
|---|---|
| `Cargo.toml` | Workspace: miembros por patrón (`core/[!.]*`, `daemons/[!.]*`, …) y `default-members` del hito 1 |
| `Cargo.lock` | Dependencias fijadas |
| `rust-toolchain.toml` | Versión del compilador |
| `cargo-config/` | Se coloca como `.cargo/` en la raíz |

`repo` los enlaza en la raíz del árbol con `<linkfile>`.

## Notas

- Edita estos archivos **solo en tu árbol de desarrollo**, nunca en el sincronizado: un cambio local hace fallar el siguiente `repo sync`.
- Todos los miembros del workspace tienen que existir en disco, así que para compilar hay que sincronizar el grupo `desktop-dev`:

```sh
repo sync -g desktop-dev
cargo check
```

## Licencia

GPL-3.0-or-later.
