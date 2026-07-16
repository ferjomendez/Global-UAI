# Prompt para Claude Code — Global UAI Website

## Contexto

Estás trabajando en el sitio web estático de **Global UAI**, una organización estudiantil de la Universidad Adolfo Ibáñez (UAI). El sitio está hosteado en **GitHub Pages** y el repo es `https://github.com/ferjomendez/Global-UAI.git`.

El sitio actual es un `index.html` con CSS y JS inline, estilo blanco y negro profesional, tipografías Playfair Display + Inter desde Google Fonts. No usa frameworks ni build tools. Los logos están en `Logos Global/`.

## Tareas

### 1. Actualizar las recomendaciones en index.html

Los estudiantes de la UAI son de nivel socioeconómico alto, NO van a lugares del centro como Tirso de Molina o La Vega. Reemplaza/agrega lugares más premium y trendy en las zonas: **Vitacura, Las Condes, Lo Barnechea, Providencia, Ñuñoa y barrios de moda**.

**Categorías a actualizar:**

- **Comida:** Restaurantes trendy y de nivel en Vitacura (Borde Río, Nueva Costanera), Las Condes, Providencia y Barrio Italia. Incluir brunch spots, sushi, cocina de autor, rooftops con comida. Eliminar Tirso de Molina, La Vega y Mercado Central.
- **Turismo:** Mantener los clásicos (Cerro San Cristóbal, Valparaíso, Cajón del Maipo) pero agregar opciones como viñedos del Valle de Casablanca, Ski en Farellones/El Colorado/Valle Nevado, Parque Bicentenario, Costanera Center Sky.
- **Bares & Pubs:** Agregar bares de Vitacura, Las Condes, Providencia. Rooftops, speakeasies, wine bars premium. Mantener los buenos de Lastarria y Bellavista.
- **Discotecas:** Agregar clubs de moda y exclusivos. Mantener La Feria y Blondie si aplican, pero sumar opciones más "top".

Investiga en la web para encontrar los mejores lugares actuales (2025-2026) en estas zonas. Cada lugar debe tener: nombre, barrio/dirección, descripción corta, y tags.

### 2. Crear páginas individuales por lugar

Cada tarjeta de recomendación en `index.html` debe linkearse a una página propia. La estructura de archivos debe ser:

```
/lugares/
  nombre-del-lugar.html
```

Usa kebab-case para los nombres de archivo (ej: `chipe-libre.html`, `la-feria.html`).

**Cada página de lugar debe incluir:**

- Navegación consistente con el sitio (nav con logo y links de vuelta al inicio)
- Nombre del lugar (h1)
- Categoría (ej: "Restaurante", "Bar", "Discoteca", "Atracción turística")
- Dirección completa
- Rating / estrellas (sobre 5, investiga el rating real en Google/TripAdvisor)
- Precio promedio por persona (en CLP, investiga precios reales)
- Rango de precio con indicador ($, $$, $$$)
- Descripción detallada (2-3 párrafos)
- Link externo al sitio web o Google Maps del lugar
- Horario de atención (si está disponible)
- Botón "Volver a recomendaciones" que regrese a la sección correspondiente en index.html
- Mantener el mismo estilo visual blanco y negro del sitio principal

**Template sugerido para las páginas de lugar:**

```html
<!-- Mantener mismo <head> con fonts y estilos del sitio principal -->
<!-- Nav con logo y link a index.html -->
<!-- Contenido del lugar con toda la info -->
<!-- Footer igual al de index.html -->
```

### 3. Actualizar las tarjetas en index.html

Cada `.rec-card` en index.html debe:
- Tener un `<a>` wrapeando la tarjeta o un botón "Ver más" que lleve a `lugares/nombre-del-lugar.html`
- Mantener el estilo actual de las tarjetas
- El hover ya existe, solo agregar el link

### 4. Push a GitHub

Cuando termines todo:

```bash
cd "C:\Users\ferjo\Desktop\Fernando Mendez\Pagina Global"
git add -A
git commit -m "Add individual place pages + update recommendations"
git push origin main
```

## Reglas de estilo

- **NO usar emojis** en el HTML
- Mantener el estilo blanco y negro profesional existente
- Tipografías: Playfair Display para títulos, Inter para cuerpo
- Animaciones sutiles con CSS (hover, transitions)
- Todo en español
- Mobile responsive
- Los estilos de las páginas de lugar pueden estar en un `<style>` dentro del mismo HTML (como el index.html actual) o en un CSS compartido — lo que sea más mantenible
- Cada página debe ser autocontenida (no depender de assets externos aparte de Google Fonts y los logos)

## Estructura final esperada

```
/
├── index.html
├── Logos Global/
│   ├── Logo normal.png
│   └── Logo normal vect.svg
└── lugares/
    ├── nombre-lugar-1.html
    ├── nombre-lugar-2.html
    ├── ...
    └── nombre-lugar-n.html
```
