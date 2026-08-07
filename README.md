# Sitio Web B2B — Instituto de Innovación Tecnológica del Perú (IIT)

Sitio estático (HTML + CSS + JS, sin dependencias de build) para la línea de
negocio de **Capacitación InHouse & Virtual para Empresas**, basado en el
Plan de Marketing IIT 2025.

## Estructura de archivos

```
/
├── index.html          → Inicio (propuesta de valor, mercado, diferenciación)
├── servicios.html       → Portafolio de capacitaciones (4 líneas de programas)
├── metodologia.html     → Proceso comercial B2B (5 etapas) + KPIs
├── nosotros.html        → Equipo, credibilidad y respaldo
├── contacto.html         → Formulario de diagnóstico gratuito + canales
├── css/styles.css       → Sistema de diseño (colores, tipografía, componentes)
├── js/main.js           → Menú móvil, animaciones y formulario
└── img/logo.png         → Logo institucional IIT
```

## Cómo subirlo a tu hosting

1. **Hosting compartido (cPanel / Plesk / cualquier hosting con FTP):**
   - Conéctate por FTP/SFTP o usa el Administrador de Archivos.
   - Sube **todo el contenido de esta carpeta** (no la carpeta en sí) dentro
     de `public_html/` (o `www/`, según tu proveedor).
   - Asegúrate de que `index.html` quede en la raíz de `public_html/`.

2. **Netlify / Vercel (arrastrar y soltar):**
   - Arrastra esta carpeta completa al panel de "Deploy" de Netlify, o
   - `vercel --prod` desde esta carpeta si usas la CLI de Vercel.

3. **GitHub Pages:**
   - Sube estos archivos a un repositorio y activa GitHub Pages apuntando
     a la rama principal (carpeta raíz).

No requiere Node.js, PHP ni base de datos — es 100% HTML/CSS/JS estático.

## Antes de publicar — pendientes a completar

- **WhatsApp:** reemplazar `+51 XXX XXX XXX` y el enlace
  `https://wa.me/51999999999` en las 5 páginas por el número real
  (formato `https://wa.me/51999999999` sin espacios ni símbolos).
- **Dominio real:** los enlaces a `www.iit.edu.pe` deben actualizarse si el
  dominio final es distinto.
- **Formulario de contacto:** el formulario de `contacto.html` funciona como
  demo visual (muestra un mensaje de confirmación en el navegador) pero
  **no envía correos todavía**. Para recibir las solicitudes reales, conecta
  el `<form id="contact-form">` a uno de estos servicios (no requieren
  backend propio):
  - [Formspree](https://formspree.io) (recomendado, plan gratuito disponible)
  - [Web3Forms](https://web3forms.com)
  - Un endpoint propio si IIT ya cuenta con backend/CRM
  El formulario ya tiene los campos `name`, `email`, `telefono`, `empresa`,
  `sector`, `interes` y `mensaje` listos para mapear a cualquiera de estos
  servicios.
- **LinkedIn:** agregar el enlace real del perfil de empresa cuando esté creado.
- **Google Analytics / Meta Pixel:** si se quiere medir tráfico y conversión
  del formulario (coherente con los KPIs digitales del plan de marketing),
  agregar el script de medición antes de `</head>` en cada página.

## Notas de diseño

- Paleta de marca: azul profundo `#0A3FA0`, cian `#00B4E8`, navy `#061B5C`,
  dorado `#C9A227` — tomada de la identidad institucional de IIT.
- Tipografías: *Space Grotesk* (títulos), *Inter* (texto), *IBM Plex Mono*
  (cifras y datos), cargadas desde Google Fonts.
- El sitio es responsive (móvil, tablet, escritorio) y usa animaciones de
  aparición progresiva al hacer scroll (con reserva: el contenido es
  visible aunque JavaScript esté deshabilitado).
- Todo el contenido (portafolio, proceso comercial, equipo, KPIs, cifras de
  mercado) proviene directamente del Plan de Marketing IIT 2025.
