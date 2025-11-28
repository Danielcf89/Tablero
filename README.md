📅 Planificador Semanal y Timer de Productividad
Una aplicación web de gestión de tareas tipo Kanban integrada directamente con Google Sheets. Permite organizar la semana, registrar el tiempo real dedicado a cada tarea y controlar las interrupciones, todo persistiendo los datos automáticamente en tu hoja de cálculo.

✨ Características Principales
Tablero Kanban Semanal: Visualización clara con columnas para "Tareas por Identificar" y los días de la semana (Lunes a Viernes).

⏱️ Timer Integrado: Cronómetro individual por tarea. Haz clic en una tarjeta para iniciar o detener el tiempo.

🔔 Contador de Interrupciones: Registra cuántas veces fuiste interrumpido durante una tarea específica.

💾 Persistencia en Google Sheets: Todas las tareas, estados, tiempos y logs se guardan en tiempo real en una Hoja de Cálculo de Google.

🖱️ Drag & Drop: Mueve las tareas entre días arrastrando y soltando.

👀 Detección de Inactividad: El timer se pausa automáticamente si cambias de pestaña o minimizas el navegador para asegurar un registro de tiempo preciso.

📊 Historial de Finalizadas: Visualización de logs con fecha, duración total e interrupciones de las tareas completadas.

🛠️ Tecnologías Utilizadas
Frontend: HTML5, JavaScript (Vanilla), Tailwind CSS (vía CDN).

Backend: Google Apps Script (.gs).

Base de Datos: Google Sheets.

🚀 Instalación y Configuración
Sigue estos pasos para desplegar tu propia versión del planificador:

1. Preparar la Hoja de Google Sheets
Crea una nueva hoja de cálculo y configura dos pestañas (hojas) con los siguientes nombres y cabeceras exactas (fila 1):

Hoja 1: Nombre Tareas (o como lo tengas definido en tu script, por defecto suele ser la hoja activa o "Hoja 1") Columnas:

ID

Nombre

Estado

Interrupciones

Tiempo_Segundos

Completada

Creada

Hoja 2: Nombre Logs Columnas:

Fecha

Dia_Finalizado

Tarea

Duracion_Segundos

Interrupciones

2. Configurar Apps Script
En tu Google Sheet, ve a Extensiones > Apps Script.

Crea dos archivos:

Code.gs: Pega aquí tu lógica de backend (funciones doGet, addTask, getTasks, etc.).

Index.html: Pega aquí todo tu código HTML/JS/CSS del frontend.

3. Desplegar como Aplicación Web
En el editor de Apps Script, haz clic en el botón azul Implementar (Deploy) > Nueva implementación.

Selecciona el tipo: Aplicación web.

Configura lo siguiente:

Ejecutar como: Yo (tu cuenta de Google).

Quién tiene acceso: Cualquiera (o Solo yo si es privado).

Haz clic en Implementar y copia la URL generada.

4. ¡Listo!
Abre la URL proporcionada y verás tu planificador funcionando conectado a tu hoja de cálculo.

📖 Cómo Usar
Agregar Tarea: Escribe el nombre en la barra superior y presiona el botón +. La tarea aparecerá en la columna "Tareas por Identificar".

Organizar: Arrastra la tarea al día de la semana correspondiente.

Trabajar: Haz clic sobre la tarjeta. Se pondrá azul y el contador empezará a correr.

Interrupciones: Si alguien te interrumpe, presiona el botón amarillo (icono de mano/pausa) arriba a la derecha.

Finalizar: Haz clic en el botón verde (check) en la tarjeta. La tarea se marcará como completada y se enviará al historial.

Eliminar: Usa el botón rojo (papelera) para borrar una tarea permanentemente.

🤝 Contribuir / Personalizar
Si quieres compartir este tablero con otra persona para que tenga sus propias tareas:

Comparte el Google Sheet en modo "Lectura" o "Editor".

Pídele que vaya a Archivo > Hacer una copia.

Esa persona deberá hacer su propio despliegue en Apps Script siguiendo los pasos de instalación.
