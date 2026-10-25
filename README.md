# Florece · Regalos digitales

App personal para componer regalos digitales con un ramo de flores, un mensaje y una apertura animada. Funciona 100 % sin internet y se puede instalar como app.

- **URL publicada:** https://mvrtinac.github.io/florece/
- **Datos:** no usa base de datos. Los regalos se guardan en IndexedDB del navegador (base `florece`), con espacio para fotos grandes y música. *Respaldar todo* descarga una copia JSON y *Restaurar* la vuelve a cargar.
- **Regalos exportados:** cada regalo se descarga como `regalo-<nombre>-<código>.html`, autocontenido. Para compartir un link en vez del archivo, el paso *Terminar* puede **publicarlo en la carpeta `regalos/` de este repo** con un token de GitHub (fine-grained, solo este repo, permiso Contents: read & write) que se guarda únicamente en tu navegador; también muestra el link y un código QR (y descarga una tarjeta QR imprimible).
- **Ramo:** flores ilustradas con detalle que se combinan y recolorean, o una fotografía propia; fondos fotográficos suaves (Pexels, licencia libre).
- **Llave y fecha:** un regalo puede pedir una clave de 4 números y/o quedarse cerrado con cuenta regresiva hasta un día y hora (según el reloj del dispositivo de quien lo abre).

## Archivos del repo

| Archivo | Para qué |
|---|---|
| `index.html` | La app completa (fuentes, estilos y lógica incluidos). |
| `manifest.json` | Nombre, colores e íconos para instalarla como app. |
| `sw.js` | Service worker: deja la app disponible sin conexión desde la URL publicada. Red primero, caché de respaldo. |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Íconos de la app. |
| `regalos/` (opcional) | Regalos exportados que quieras compartir por link. |

Todas las rutas son relativas, así que el repo puede llamarse como quieras.

## Publicar un cambio

1. Reemplaza los archivos en GitHub y haz commit.
2. Espera 5-10 minutos (caché de GitHub Pages).
3. Prueba en una ventana de incógnito. Si una pestaña vieja no se actualiza, recárgala una vez más: el service worker baja la versión nueva en la primera carga y la muestra en la siguiente.

Fuentes incrustadas: Lora y Poppins (SIL Open Font License). Arte, nombre y animaciones originales.
