# Germy Services

Sitio web y material de venta para **Germy Services** — desarrollo de páginas web para comercios de Burzaco y Zona Sur (Buenos Aires).

## Propósito

Convertir búsquedas en Google y redes sociales en consultas directas por WhatsApp para comercios, oficios y profesionales de la zona. El sitio vende 4 paquetes: Presencia local, Catálogo que consulta, Turnos o reservas, y Tienda online.

## Contenido del repo

| Archivo | Descripción |
| :-- | :-- |
| `index.html` | Landing page completa (HTML + CSS inline, sin dependencias). Incluye: hero, servicios, 4 paquetes con precios, proceso de trabajo, demos en vivo, FAQ, contacto y SEO local (JSON-LD `LocalBusiness`). |
| `documentos/referencia_de_desarrollo.md` | Guía operativa de venta e implementación: fases (detección → diagnóstico → propuesta → implementación → postventa), preguntas guía, checklist de QA, plantillas de contacto y plan de arranque. |

## Despliegue

El sitio está publicado en GitHub Pages: https://germyc.github.io/germy_services/

## Stack

- HTML5 + CSS3 (custom properties, grid, responsive)
- Sin frameworks ni build step
- JSON-LD para SEO local
- WhatsApp CTA con mensaje pre-cargado

## Uso

Abrir `index.html` directamente en el navegador o servir con cualquier servidor estático:

```bash
npx serve .
# o
python -m http.server 8000
```
