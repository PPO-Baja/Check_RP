Mi Formulario (PWA) — PWA wrapper para Microsoft Forms

Cómo usar:
1) Abre el archivo 'index.html' y reemplaza la constante FORMS_URL por tu enlace real de Microsoft Forms.
   - Idealmente usa el parámetro '?embed=true' en tu URL.
   - Ejemplo: const FORMS_URL = "https://forms.office.com/Pages/ResponsePage.aspx?id=XXXX&embed=true";

2) Sube la carpeta completa a un hosting estático (GitHub Pages, Netlify, Vercel, Azure Static Web Apps, etc.).
   - En GitHub Pages, coloca los archivos en la rama 'gh-pages' o habilita Pages para la rama principal.
   - Asegúrate de que 'sw.js' esté servido desde la raíz del sitio (ruta '/sw.js') como en este proyecto.

3) Abre el sitio desde tu teléfono y usa "Añadir a la pantalla de inicio" para instalar el PWA.

Notas:
- Si tu organización bloquea el 'embedding' del formulario (X-Frame-Options), la app mostrará un aviso con un enlace para abrirlo en una pestaña nueva.
- El Service Worker proporciona un 'shell' offline mínimo (pantalla de "Sin conexión"). Microsoft Forms requiere internet para funcionar.
- Personaliza iconos en /assets si deseas tus propios gráficos (se incluyen iconos genéricos por defecto).
