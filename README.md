# Ruta de inglés B2.1 → C1

Plan de estudio interactivo de 20 semanas (12 oct 2026 – 28 feb 2027), tres días por semana,
orientado a psicología, defensa de derechos humanos y comunicación profesional.

Página estática, sin dependencias ni backend. El avance, las notas y el glosario se guardan
en el `localStorage` del navegador de quien la usa: no viajan a ningún servidor, pero tampoco
se sincronizan entre dispositivos.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | La página completa: estilos, contenido y lógica en un solo archivo |
| `.nojekyll` | Evita que GitHub Pages procese el sitio con Jekyll |

## Publicar en GitHub Pages

Repositorio: `pcastroc/NataliaCastro`.

1. Sube `index.html`, `README.md` y `.nojekyll` a la **raíz** del repositorio.
   Desde la web: **Add file → Upload files**, arrastra los tres y **Commit changes**.
2. Entra a **Settings → Pages**.
3. En **Source** elige `Deploy from a branch`; en **Branch**, `main` y carpeta `/ (root)`. Guarda.
4. Espera uno o dos minutos. La página queda en:

   ```
   https://pcastroc.github.io/NataliaCastro/
   ```

El repositorio debe ser **público** para que Pages funcione en el plan gratuito.

Si prefieres hacerlo por consola:

```bash
git clone https://github.com/pcastroc/NataliaCastro.git
cd NataliaCastro
# copia aquí index.html, README.md y .nojekyll
git add .
git commit -m "Ruta de inglés B2.1 a C1 para Natalia"
git push origin main
```

Después activa Pages con los pasos 2 a 4.

## Modificar el plan

Todo el contenido vive en el bloque `<script>` al final de `index.html`:

- `L` — los enlaces externos, en un solo sitio.
- `PLAN` — los cinco meses, sus semanas y las tres tareas de cada semana.
  Cada tarea necesita un `id` único (es la llave con la que se guarda el avance),
  un `day`, un `text` y, opcionalmente, `url` + `go` para el enlace,
  y `tag` con `tagType: "cert"` o `"word"` para la etiqueta de color.
- `CERTS` y `TOOLS` — las tablas de certificados y de herramientas.

Las fechas `start` y `end` de cada semana son las que encienden el distintivo
«esta semana» cuando corresponde.

> Al cambiar un `id` de tarea se pierde el avance ya marcado de esa tarea.
> Si alguna vez rehaces el plan entero, sube también la versión en la constante `KEY`
> (`ruta-c1-estefanie-v2` → `v3`) para empezar con el tablero limpio.

## Colores

Paleta oro rosa, negro, blanco y rojo, definida como variables CSS en `:root`,
con su equivalente para modo oscuro. Cambiar un color es cambiar una línea.
