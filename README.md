# munchManager Bot de Monitorización de Telegram

Este bot de Telegram monitoriza mensajes en grupos para verificar si los usuarios han enviado al menos un mensaje que contenga una palabra clave configurada.

## Funcionalidades

- Configurar una palabra clave para cada grupo
- Registrar mensajes de usuarios y verificar si contienen la palabra clave
- Mantener una lista de usuarios "missing" (que no han usado la palabra clave)
- Responder al comando `/missing` con la lista de usuarios missing (solo administradores)
- Responder al comando `/presentacion <usuario>` para mostrar el último mensaje con la palabra clave de un usuario
- Guardar datos persistentes en archivos JSON

## Instalación

1. Clona este repositorio
2. Instala las dependencias con `pip install -r requirements.txt`
3. Crea un archivo `.env` con tu token de bot de Telegram (`TELEGRAM_BOT_TOKEN=tu_token_aquí`)
4. Ejecuta el bot con `python main.py`

## Uso

1. Agrega el bot a un grupo
2. Configura la palabra clave con `/setword <palabra>`
3. El bot monitorizará los mensajes automáticamente
4. Usa `/missing` para obtener la lista de usuarios que no han usado la palabra clave
5. Usa `/presentacion <usuario>` para obtener el último mensaje de un usuario que contiene la palabra clave

## Estructura del Proyecto

- `main.py`: Punto de entrada principal
- `config.py`: Gestión de configuración
- `handlers/`: Manejadores de comandos y mensajes
- `models/`: Modelos de datos y lógica de negocio
- `utils/`: Utilidades y funciones auxiliares
- `data/`: Directorio donde se guardan los archivos JSON
