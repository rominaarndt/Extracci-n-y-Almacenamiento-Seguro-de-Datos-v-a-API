# YouTube Channel Data Extractor 🚀

Este proyecto es un script en Python diseñado para consultar la API oficial de **YouTube Data API v3** y obtener metadatos clave de un canal de YouTube utilizando su *handle* (por ejemplo, `@mouredev`). Los resultados se procesan y se guardan de forma estructurada en un archivo local en formato JSON.

## 📋 Características

*   **Extracción automática:** Recupera estadísticas en tiempo real (suscriptores, reproducciones totales, cantidad de videos, país, etc.).
*   **Gestión segura de credenciales:** Utiliza un archivo `.env` para evitar exponer públicamente tu clave de API de Google.
*   **Salida estructurada:** Guarda la información de forma limpia y formateada en un archivo llamado `mouredev_channel_data.json`.

## 🛠️ Requisitos e Instalación

Antes de ejecutar el script, asegúrate de tener instaladas las dependencias necesarias. Puedes instalarlas ejecutando:

```bash
pip install requests python-dotenv
```

## 🔑 Configuración de la API Key

1. Obtén una clave de API desde la consola de [Google Cloud Console](https://console.cloud.google.com/) habilitando la **YouTube Data API v3**.
2. Crea un archivo llamado `.env` en la raíz de tu proyecto.
3. Añade tu API key al archivo con el siguiente formato:

```env
YOUTUBE_API_KEY="TU_API_KEY_AQUI"
```

## 🚀 Uso

Ejecuta el script principal para realizar la consulta e importar los datos:

```python
python main.py
```

## 📊 Ejemplo de Estructura de Datos (JSON)

El archivo de salida `mouredev_channel_data.json` tendrá una estructura similar a la siguiente:

```json
{
    "channel_id": "UCxPD7bsocoAMq8Dj18kmGyQ",
    "titulo": "MoureDev by Brais Moure",
    "descripcion": "Aprende programación e Inteligencia Artificial desde cero...",
    "custom_url": "@mouredev",
    "fecha_creacion": "2014-07-06T15:43:32Z",
    "pais": "ES",
    "suscriptores": "1020000",
    "vistas_totales": "67157851",
    "videos_totales": "1120"
}
```

---
Creado con ❤️ para automatizar el análisis de canales de YouTube.
