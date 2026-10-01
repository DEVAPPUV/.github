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

Nunca trabajes directo en `main`.

```bash
git checkout main
git pull origin main
git checkout -b feature/pantalla-login
```

| Prefijo | Para qué |
|---|---|
| `feature/` | Funcionalidad nueva |
| `fix/` | Corrección de un error |
| `docs/` | Solo documentación |
| `refactor/` | Mejora interna sin cambiar el comportamiento |

## 3. Haz commits pequeños y claros

Mensaje en español, en presente, diciendo **qué** hace el cambio:

```
Agrega bloqueo temporal tras intentos fallidos de login
Corrige error de métricas en Mi actividad
Documenta variables de entorno del backend
```

## 4. Abre un Pull Request

- Base: `main`. Compara con tu rama.
- Completa la plantilla que aparece.
- En la descripción escribe `Closes #12` (o `Closes DEVAPPUV/appano-backend#12` si el issue está en otro repo). Así el issue se cierra solo al unir.
- Pide revisión a otra persona. Muévela a **In review**.

## 5. Revisión

- Al menos **una aprobación** antes de unir.
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
