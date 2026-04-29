Despliegue rápido en Vercel

1) Requisitos
- Cuenta en Vercel (https://vercel.com)
- Git (recomendado) o la CLI de Vercel

2) Estructura del proyecto
- `carta_invitacion_mama.html` (archivo principal)
- `foto_mama.jpeg` (imagen en la misma carpeta)

3) Desplegar (opción rápida con la CLI)
- Instala Vercel CLI:

```bash
npm i -g vercel
```

- Desde la carpeta del proyecto (donde está `carta_invitacion_mama.html` y `foto_mama.jpeg`) ejecuta:

```bash
vercel
```

- Sigue el asistente (login / seleccionar equipo / confirmar). Al final obtendrás una URL pública, por ejemplo `https://mi-invitacion.vercel.app`.

4) IMPORTANTE: actualizar meta `og:image`
- Para que la vista previa en WhatsApp muestre la imagen correcta, edita `carta_invitacion_mama.html` y reemplaza `{DEPLOY_URL}` por la URL pública que te entregó Vercel.
  - Ejemplo: `https://mi-invitacion.vercel.app/foto_mama.jpeg`

5) Verificar la vista previa en WhatsApp
- WhatsApp usa su propio caché. Tras actualizar `og:image` y desplegar, comparte la URL en un chat o usa el validador de Facebook (Sharing Debugger) para forzar refresco: https://developers.facebook.com/tools/debug/
- Pega la URL pública (ej. `https://mi-invitacion.vercel.app`) y presiona "Depurar" y luego "Scrape Again" para actualizar la caché.

6) Opcional: usar GitHub + Vercel
- Inicializa repo, sube a GitHub y conecta el repo en Vercel para despliegues automáticos al hacer push.

Si quieres, puedo:
- Crear `vercel.json` con configuraciones básicas.
- Actualizar automáticamente `og:image` cuando me pases la URL de despliegue.
- Hacer el commit y (si me das acceso) intentar desplegar por ti.
