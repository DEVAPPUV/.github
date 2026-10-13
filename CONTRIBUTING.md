# Guía para contribuir a Appaño

Gracias por sumarte. Esta guía vale para los tres repositorios de la organización.

## El flujo en una línea

**Issue → rama → commits → Pull Request → revisión → merge → el issue se cierra solo.**

## 1. Parte siempre desde un issue

Todo trabajo tiene un issue. Las tareas están en el **Project "Appaño"** y cuelgan de una historia de usuario (HU) en `appano-planificacion`. Antes de empezar:

1. Elige una tarea del tablero y asígnatela.
2. Muévela a **In progress**.
3. Si la tarea necesita un cambio en el otro lado (back ↔ front), revisa el **contrato de la API** descrito en la HU. Si cambia, avisa en el issue **antes** de seguir.

## 2. Crea una rama

Usamos **Gitflow** en `appano-backend`, `appano-frontend` y `appano-planificacion`: `main` guarda solo lo publicado y `develop` integra el trabajo. Nunca trabajes directo en `main` ni en `develop`.

La primera vez, en cada repo, configura git-flow con `git flow init` (producción `main`, desarrollo `develop`, prefijos por defecto y prefijo de tags `v`). Luego, para cada historia:

```bash
git checkout develop
git pull
git flow feature start HU-03-crear-reporte
```

| Prefijo | Para qué | Nace de |
|---|---|---|
| `feature/HU-XX-...` | Una historia de usuario (incluye su documentación y refactor) | `develop` |
| `bugfix/` | Error encontrado en `develop` (aún no publicado) | `develop` |
| `release/X.Y.0` | Preparar una entrega | `develop` |
| `hotfix/X.Y.Z` | Error urgente en la app publicada | `main` |

Los pasos de release y hotfix están en el [flujo de trabajo](https://github.com/DEVAPPUV/appano-planificacion/blob/develop/docs/flujo-de-trabajo.md#ramas-y-pull-requests-gitflow).

## 3. Haz commits pequeños y claros

Mensaje en español, en presente, empezando por la HU y diciendo **qué** hace el cambio:

```
HU-01: Agrega bloqueo temporal tras intentos fallidos de login
HU-04: Corrige error de métricas en Mi actividad
HU-10: Muestra la versión de la app y el contacto
```

## 4. Abre un Pull Request

- Base: **`develop`**. Compara con tu rama. Solo los `release/` y `hotfix/` van a `main`.
- Completa la plantilla que aparece.
- En la descripción escribe `Closes #12` (o `Closes DEVAPPUV/appano-planificacion#12` para cerrar una HU, que vive en otro repo). Así el issue se cierra solo al unir.
- No uses `git flow feature finish`: une la rama sin revisión. El cierre siempre es con PR.
- Pide revisión a otra persona. Muévela a **In review**.

## 5. Revisión

- Al menos **una aprobación** antes de unir.
- Cada integrante trabaja con **su propia cuenta** de GitHub. **Nadie aprueba ni une su propio PR.**
- Se une con **"Merge pull request"** (squash y rebase están desactivados).
- Quien revisa mira que se cumplan los **criterios de aceptación** del issue y la **Definición de Terminado** de la HU.
- Los comentarios se resuelven en el mismo PR.

## Definición de Terminado (común a todas las tareas)

- [ ] Código revisado y aprobado por al menos una persona.
- [ ] Pruebas del flujo en verde (cuando existan).
- [ ] Sin datos sensibles (contraseñas, tokens, respuestas secretas) en logs ni en el código.
- [ ] Validado en Android e iOS (tareas de la app).
- [ ] Documentación actualizada si cambió algo que otra persona necesite saber.

## Reglas de oro de seguridad

1. **Nunca subas** `.env`, claves, respaldos de base de datos ni datos reales. Usa `.env.example` con nombres de variables sin valores.
2. **Datos de prueba falsos**, siempre.
3. Si subiste un secreto por error, avísalo de inmediato. Hay que cambiarlo, no basta con borrarlo.
4. Ante la duda sobre si algo es sensible, trátalo como si lo fuera.

## Etiquetas

| Etiqueta | Significado |
|---|---|
| `historia-de-usuario` | Issue padre, vive en `appano-planificacion` |
| `backend` / `frontend` / `ux` / `contenido` | A quién le toca |
| `hallazgo` | Algo que hoy **no** se cumple y se detectó en el diagnóstico |
| `prioridad-alta` / `prioridad-media` / `prioridad-baja` | Orden de atención |
| `bug` | Error en algo que ya existía |

## Dudas

Abre un issue en `appano-planificacion` o comenta en la HU correspondiente.
