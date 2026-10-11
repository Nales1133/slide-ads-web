# Página de Sliders

Página para la prueba de interés: video, cómo funciona y formulario para apuntarse.

## Archivos
- `index.html`: la página.
- `privacidad.html`: política de privacidad (Ley 1581).
- `video/slide-ads.mp4`: el video corto de Slide.
- `video/slidy.mp4`: el video de Slidy y Bizy.
- `slidy/index.html`: el juego Slidy, jugable en celular y computador (se abre en `.../slide-ads-web/slidy/`).
- `radio/`: las 8 pistas de la Radio de Spily, los 5 segmentos «Spily al aire» y las 9 frases de la emisora (MP3). Las portadas se dibujan en la página, no son archivos.
- `img/`: icono, imagen del video y la imagen que se ve al compartir el enlace.

## Lo único que hay que editar
Al final de `index.html`:
```
var FORM_URL = '';          // pega aquí el enlace de tu formulario de Tally
var CONTACTO = '...';       // tu correo
```

## Activar TagSlider (muro de tags)
Los tags se guardan en un Formulario de Google conectado a una Hoja de cálculo. Gratis y sin servidor.

1. En forms.google.com crea un formulario llamado «TagSlider» con 3 preguntas de **respuesta corta**, en este orden:
   - `Nombre`
   - `Comentario` (puede ser de párrafo)
   - `Personaje`
2. En **Configuración**, desactiva «Recopilar correos electrónicos» y que no pida iniciar sesión.
3. Menú ⋮ → **Obtener enlace prellenado**. Escribe cualquier cosa en las 3 preguntas (por ejemplo a, b, c), toca **Obtener enlace** y cópialo.
4. Pestaña **Respuestas** → **Vincular a Hojas** → crea la hoja.
5. En la hoja, escribe `Ocultar` como título de la primera columna vacía (después de Personaje).
6. **Compartir** → Acceso general: «Cualquier persona con el enlace» como **Lector**. Copia el enlace de la hoja.
7. Al final de `index.html` pega los dos enlaces:
```
var TAG_FORM = 'el enlace prellenado del paso 3';
var TAG_SHEET = 'el enlace de la hoja del paso 6';
```

**Moderar:** abre la hoja. Para quitar un tag escribe una `x` en su columna **Ocultar** (o borra la fila). Desaparece de la página en menos de un minuto.
Mientras los enlaces estén vacíos, TagSlider funciona en modo de prueba: los tags solo se ven en el navegador de quien los escribe.
