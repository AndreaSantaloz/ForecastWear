# ForecastWear
## Creadora
Andrea Santana López
---

# 👗 Asesor de Outfits Inteligente (ForecastWear) pero el asesor se llama Brigit

Este proyecto es una aplicación web interactiva construida con **Gradio** que utiliza Inteligencia Artificial para analizar tu vestimenta, detectar el clima actual de tu ubicación y ofrecerte una recomendación personalizada sobre si tu outfit es adecuado o no.

## ✨ Características

* **Segmentación Semántica:** Identifica y separa automáticamente las prendas de una imagen (pantalones, camisas, vestidos, zapatos, etc.) usando `SegFormer`.
* **Clasificación Específica:**
* **Ropa:** Clasifica el tipo de prenda (Blusa, Vaqueros, Suéter, etc.).
* **Calzado:** Modelo especializado para distinguir entre Deportivas, Mocasines, Botas y más.


* **Geolocalización y Clima:** Detecta automáticamente tu ciudad mediante IP y obtiene la temperatura y estado del cielo en tiempo real con la API de `Open-Meteo`.
* **Asesor de Estilo:** Genera una recomendación basada en el contexto (hora, clima y prendas detectadas).

---

## 🛠️ Requisitos Previos

Antes de empezar, asegúrate de tener instalado:

* **Python 3.9** o superior.
* Acceso a internet (para descargar los modelos de Hugging Face y consultar el clima).

---

## 🚀 Instalación y Configuración

Sigue estos pasos para ejecutar la aplicación en tu máquina local:

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/nombre-del-repo.git
cd nombre-del-repo

```

### 2. Crear un entorno virtual (Recomendado)

```bash
python -m venv venv
# En Windows:
venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate

```

### 3. Instalar las dependencias

Necesitarás instalar las librerías de procesamiento de imagen, modelos de IA y la interfaz:

```bash
pip install gradio numpy torch torchvision pillow requests transformers deep-translator

```

### 4. Ejecutar el servidor de recomendaciones (Opcional/Configurable)

El código busca un servicio de recomendación en `http://localhost:8000/recommend`.

> **Nota:** Si no tienes este microservicio externo funcionando, la app mostrará "No se pudo obtener recomendación", pero el análisis de imagen y clima seguirá funcionando perfectamente.

### 5. Iniciar la aplicación

Aviso hay que ejecutar el archivo server.ipynb para que el servidor LLM te haga las recomendaciones.

Una vez ejecutado, verás un enlace local . Ábrelo en tu navegador.

---

## 📖 Cómo usar la App

1. **Sube una foto** donde se vea claramente tu outfit completo.
2. Haz clic en el botón **"Analizar Outfit"**.
3. **Resultados:**
* A la izquierda verás la imagen con las prendas coloreadas (máscaras de segmentación).
* Se abrirá una galería con cada prenda recortada y su nombre detectado.
* A la derecha verás los datos del clima de tu zona y la recomendación final.



---

## 🧪 Tecnologías utilizadas

* **Gradio:** Para la interfaz de usuario.
* **Hugging Face Transformers:** Modelos `SegFormer` y `Siglip`.
* **PyTorch:** Motor de los modelos de Deep Learning.
* **Open-Meteo API:** Datos meteorológicos gratuitos.
* **Deep Translator:** Traducción automática de ubicaciones.

---

