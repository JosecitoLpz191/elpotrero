# Rancho Ganadero — PWA inicial

Aplicación web progresiva (PWA) de administración local de ganado bovino. Diseñada para desarrollarse desde Windows y usarse en iPhone mediante Safari.

## Funciones incluidas
- Fichas de animales: número de arete único, apodo, raza, color, fecha de nacimiento/edad calculada, sexo, estado, peso, foto, observaciones, madre y padre.
- Relación madre-cría y listado de crías en la ficha de la vaca.
- Salud: vacunas, desparasitación, enfermedades, medicamentos, revisiones, dosis, fecha, próxima fecha, estado, notas y costo.
- Finanzas: ingresos, gastos, categorías, montos en MXN, animal relacionado y balance.
- Búsqueda, filtros, actividad reciente, almacenamiento IndexedDB, respaldo JSON y modo sin conexión.
- Sin cuenta, analítica ni backend: los datos se quedan en el almacenamiento local de cada navegador/dispositivo.

## Probar en Windows
1. Extrae el ZIP.
2. Abre la carpeta extraída en el Explorador de archivos, haz clic en la barra de dirección, escribe `cmd` y pulsa Enter.
3. Ejecuta `py -m http.server 8000`.
4. Abre `http://localhost:8000` en el navegador.

No abras `index.html` con doble clic: el Service Worker requiere localhost o HTTPS.

## Publicar para usarlo en iPhone
Publica los archivos en un hosting estático con HTTPS, por ejemplo GitHub Pages o Cloudflare Pages. Después abre el enlace en Safari y selecciona Compartir → Añadir a pantalla de inicio. Abre la app una vez conectada y prueba el modo avión.

## Importante
- No se sincronizan datos entre usuarios o teléfonos.
- El almacenamiento local no tiene cifrado propio; protege el dispositivo y evita guardar datos extremadamente sensibles.
- Exporta respaldos regularmente. El respaldo JSON contiene tus datos e imágenes; guárdalo de forma segura.
- El costo de un registro de salud también crea un movimiento de gasto automáticamente. Evita duplicarlo manualmente en Finanzas.
- Los registros sanitarios no sustituyen las indicaciones de un veterinario.
- Esta es una versión inicial; pruébala con pocos registros antes de usarla como registro principal del rancho.
