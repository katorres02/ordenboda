# Distribución de Boda 💍

Sitio web interactivo para organizar los asientos de la boda. Todo en un solo archivo
(`index.html`), **sin dependencias externas** → funciona sin internet y se publica
directo en GitHub Pages.

## Cómo usarlo

- Pestañas **Ceremonia** y **Cena** (mesa en U).
- **Toca un invitado** de la lista "Sin asignar" y luego **toca un asiento** para sentarle.
  También puedes **arrastrar** los invitados a los asientos (en computadora).
- Toca un asiento ocupado para "levantar" a esa persona y moverla.
- Arrastra un invitado de vuelta a la lista para dejar su asiento libre.
- **⚙︎ Ajustar distribución**: cambia el número de sillas/filas de cada sección.
- **＋ Añadir invitado** y la **×** en cada invitado para quitarlo de la lista.
- **🖨 Imprimir / PDF** para tener la distribución en papel.
- Los cambios se **guardan automáticamente** en el navegador del dispositivo.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (p. ej. `ordenboda`).
2. Sube este archivo `index.html` (y este README):
   ```bash
   git init
   git add index.html README.md
   git commit -m "Distribución de boda"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/ordenboda.git
   git push -u origin main
   ```
3. En GitHub → **Settings → Pages** → *Build and deployment* → Source: **Deploy from a branch**,
   Branch: **main** / **/ (root)** → Save.
4. En 1–2 minutos estará en `https://TU-USUARIO.github.io/ordenboda/`.

> Nota: la distribución se guarda en cada dispositivo por separado (localStorage). Si quieres
> que todos vean exactamente la misma distribución, edita los valores por defecto en
> `defaultState()` dentro de `index.html`.
