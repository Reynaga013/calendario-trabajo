# Calendario de Trabajo

App de una sola página (sin build) para apuntar clientas de limpieza, horas
trabajadas y lo que se cobra cada día, organizado como un calendario
mensual. Para usarla hace falta entrar con una cuenta (correo y
contraseña) — los datos se guardan en Firebase (Firestore), así que viven
en la nube y no se pierden si se borra el navegador, se resetea el móvil o
se cambia de teléfono: basta con entrar con la misma cuenta en el nuevo
dispositivo. También se guarda una copia local en el propio móvil para
poder seguir viendo/apuntando cosas sin conexión, que se sincroniza sola en
cuanto vuelve el internet.

## Publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (puede ser público, no hace falta
   plan de pago para usar Pages).
2. Sube el contenido de esta carpeta a la raíz del repositorio: `index.html`,
   `manifest.json` y la carpeta `icons/`.
3. Ve a **Settings → Pages**. En "Source" elige **Deploy from a branch**,
   rama `main` y carpeta `/ (root)`. Guarda.
4. Espera uno o dos minutos — GitHub te da un enlace del tipo
   `https://tu-usuario.github.io/nombre-del-repo/`. Ese es el link que le
   pasas.

## Instalarla en el móvil

1. Abre ese enlace en el móvil (Chrome en Android o Safari en iPhone).
2. Toca el menú del navegador → **"Añadir a pantalla de inicio"**
   (Android) o **Compartir → "Añadir a pantalla de inicio"** (iPhone).
3. Queda como un icono más, con el logo del calendario, y se abre a
   pantalla completa como una app — sin barra del navegador.

## Copia de seguridad

Dentro de la app, el icono de ajustes (arriba a la derecha) tiene
**"Exportar copia de seguridad"**, que descarga un archivo `.json` con todo
lo apuntado, y **"Importar copia de seguridad"** para recuperarlo si alguna
vez cambia de móvil o borra los datos del navegador por error. Conviene
exportar una copia de vez en cuando (por ejemplo, guardándola en Drive o
enviándosela a otra persona por WhatsApp) — al vivir solo en el
almacenamiento del navegador, no hay ninguna otra copia en ningún sitio.

## Icono

`icons/icon.svg` es el icono fuente (dibujado a mano, no generado por IA):
una página de calendario blanca sobre un degradado azul, con un cuadradito
verde que representa un día ya apuntado. `icons/icon-maskable.svg` es la
misma imagen encogida al 66% y centrada, para que Android no la recorte mal
al aplicarle su máscara circular/redondeada. El resto de PNG/ICO de la
carpeta `icons/` están generados a partir de esos dos SVG y no hace falta
tocarlos a mano.

## Actualizar la app más adelante

Es un único archivo `index.html` con el CSS y el JS dentro — para cambiar
cualquier cosa (textos, colores, alguna función), basta con editar ese
archivo y volver a subirlo al repositorio; GitHub Pages actualiza el sitio
solo en cuanto detecta el cambio.
