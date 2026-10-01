<div align="center">

# Appaño

**Reporte anónimo y seguro de violencias de género en la región de Valparaíso**

![Plataformas](https://img.shields.io/badge/plataformas-Android%20%7C%20iOS-4c8bf5)
![Madurez](https://img.shields.io/badge/madurez-TRL%203%20%E2%86%92%20TRL%204-8a63d2)
![Cobertura](https://img.shields.io/badge/cobertura-38%20comunas-2ea44f)

</div>

---

## ¿Qué es Appaño?

Appaño es una **aplicación móvil** (Android e iOS) que permite **reportar de manera anónima** situaciones de violencia de género vividas o presenciadas en las **38 comunas de la región de Valparaíso**, y que entrega información clara sobre **tipos de violencia, derechos y canales de apoyo y denuncia**.

Fue co-diseñada en el proyecto Anillo ANID **"Descentrando las desigualdades de género"** (ATE220051) de la Universidad de Valparaíso, junto a la ciudadanía, mediante talleres en el Gran Valparaíso, Quillota y Rapa Nui. Es la puerta de entrada de datos del futuro **Observatorio Ciudadano de Desigualdades de Género**.

## ¿Por qué importa?

Existe una brecha entre quienes viven violencia de género y quienes llegan a denunciar. Según la Encuesta Nacional de Violencia contra las Mujeres 2024, en la región de Valparaíso el 19,2 % de las mujeres declaró haber vivido violencia y solo el 30 % de ellas hizo una denuncia formal. La vergüenza, el miedo a represalias y la desconfianza en las instituciones pesan más que la falta de información.

Appaño busca ser un **primer paso seguro**: reconocer lo ocurrido, registrarlo sin exponerse y saber a dónde acudir. A la vez, genera información agregada y actualizada que hoy escasea para diseñar políticas de prevención y acompañamiento.

## ¿Cómo funciona?

| | Qué puede hacer una persona usuaria |
|---|---|
| 📖 **Informarse** | Conocer los tipos de violencia y encontrar centros de apoyo filtrados por su comuna, con dirección, horario y contacto. |
| 📝 **Reportar** | Registrar una situación con o sin cuenta. Un reporte hecho sin iniciar sesión **no queda vinculado a ninguna persona**. |
| 📊 **Hacer seguimiento** | Ver sus reportes y gráficos con datos agregados en "Mi actividad". |
| 🔐 **Cuidar su cuenta** | Recuperar el acceso (correo o pregunta secreta), cambiar la contraseña o eliminar la cuenta conservando el anonimato de sus reportes. |

## Principios de diseño

- **Anonimato por diseño:** el sistema no necesita saber quién reporta.
- **Mínimos datos personales:** solo se guarda lo necesario para operar.
- **Seguridad primero:** se maneja información sensible, así que la seguridad y la privacidad pesan más que la velocidad de desarrollo.
- **Información verificada:** los contenidos y los centros de apoyo se validan con el equipo de DesCentrando.

## ¿En qué estamos trabajando ahora?

Appaño ya funciona como **prototipo (TRL 3)**. Hoy avanzan en paralelo dos líneas:

1. **Validación en terreno** (Concurso innovANDO 2030, Universidad de Valparaíso): piloto controlado con estudiantes, funcionariado y cuerpo académico para pasar a **TRL 4** (prototipo validado en entorno relevante). Se evalúa aceptación, usabilidad y carga cognitiva.
2. **Evaluación y mejora técnica del sistema** (trabajo de título, Ingeniería Informática): auditoría de calidad y arquitectura, corrección de defectos y refuerzo de seguridad.

### Hoja de ruta

| Etapa | Período estimado | Resultado esperado |
|---|---|---|
| Diagnóstico funcional | Oct 2026 | Casos de prueba y catastro de defectos |
| Evaluación de arquitectura | Nov 2026 | Informe de arquitectura, análisis de código y propuesta priorizada de mejoras |
| Implementación de mejoras | Mar – May 2027 | Backend refactorizado y pruebas automatizadas |
| Validación con usuarias | May – Jun 2027 | Informe de usabilidad, aceptación y carga mental |
| Cierre | Jun – Jul 2027 | Memoria y paquete de código auditado y transferible |

> Las fechas son estimadas y pueden ajustarse.

## Dónde está cada cosa

| Repositorio | Para qué sirve |
|---|---|
| **appano-planificacion** | Historias de usuario, tareas y documentación del proyecto. **Empieza por aquí.** |
| **appano-backend** | API REST (Node.js + Express) y base de datos (MariaDB/MySQL). |
| **appano-frontend** | Aplicación móvil (React Native + Expo). |

El avance de todas las tareas se ve en un solo tablero: el **Project "Appaño"** de esta organización (pestaña *Projects*).

## Seguridad y privacidad de este espacio

- Los repositorios son privados.
- **Nunca** se suben credenciales, archivos `.env`, respaldos de la base de datos ni datos de personas usuarias.
- Si encuentras una vulnerabilidad, lee [SECURITY.md](https://github.com/DEVAPPUV/.github/blob/main/SECURITY.md) y avísanos de forma privada.

## Créditos e institucionalidad

- **Universidad de Valparaíso**: titular de la propiedad intelectual. Appaño está registrada como programa de computación a nombre de la universidad.
- **Proyecto Anillo ANID "Descentrando las desigualdades de género"** (ATE220051): origen y co-diseño de la aplicación.
- **Concurso innovANDO 2030** (Conocimiento 2030): financia la validación y el fortalecimiento de Appaño.
- **Beneficiarias directas:** comunidad estudiantil, académica y funcionaria de la Universidad de Valparaíso. **Indirectas:** instituciones públicas de prevención y abordaje de la violencia de género (por ejemplo SERNAMEG y municipios) y otras universidades interesadas en implementar la herramienta.
