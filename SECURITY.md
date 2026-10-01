# Política de seguridad

Appaño maneja información sensible sobre situaciones de violencia de género. Tomamos en serio cualquier falla que pueda exponer datos o comprometer el anonimato de las personas usuarias.

## Cómo reportar una vulnerabilidad

**No abras un issue público.** Escríbenos de forma privada:

- Correo: ⚠️ COMPLETAR: correo de contacto del equipo
- O usa la opción **Security → Report a vulnerability** del repositorio afectado.

Incluye, si puedes:

1. Qué encontraste y en qué parte (app, API, base de datos).
2. Pasos para reproducirlo.
3. Qué información podría quedar expuesta.

Intentaremos responder en un plazo de 5 días hábiles.

## Qué hacer si encuentras datos sensibles en un repositorio

Si ves una contraseña, un token, un `.env` o datos reales de personas usuarias:

1. No los copies ni los compartas.
2. Avísanos por el canal privado de arriba.
3. Cambiaremos las credenciales expuestas de inmediato. Borrar el archivo no basta, porque el historial de Git lo conserva.

## Buenas prácticas para quien contribuye

- Usa solo **datos de prueba falsos**, nunca datos reales.
- Mantén el ambiente de pruebas separado del de producción.
- No imprimas contraseñas, tokens ni respuestas secretas en los logs.
- Si dudas de si algo es sensible, trátalo como si lo fuera.
