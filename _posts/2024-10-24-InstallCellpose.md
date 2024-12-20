---
title: Cellpose
date: 2024-10-24
categories:
- Cellpose
excerpt: |
  Guía de instalación de Cellpose v3 con Anaconda.
feature_text: |
  ## Guía de instalación de Cellpose v3
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

Cellpose es una herramienta de segmentación de imágenes basada en inteligencia artificial (IA) diseñada para identificar células en imágenes biomédicas, especialmente en microscopía. Desarrollada inicialmente en el laboratorio de Branton Lee y Charles E. Boone, su propósito es proporcionar una herramienta automatizada, accesible y precisa para la investigación biológica y médica.

Consulta más información en:  
- **Documentación oficial**: [Cellpose Docs](https://cellpose.readthedocs.io/en/latest/)  
- **Repositorio GitHub**: [Cellpose GitHub](https://github.com/MouseLand/cellpose/blob/main/)

---

### ¿Qué es Anaconda?

Anaconda es una distribución de software libre que incluye herramientas para ciencia de datos y aprendizaje automático, facilitando la administración de paquetes y entornos de Python y R.

---

### Instalación de Cellpose v3 GUI utilizando Anaconda

Para este taller, utilizaremos la interfaz gráfica (GUI) de Cellpose instalada de manera local. También es posible trabajar con sus versiones online:  
- **[Cellpose Online](https://www.cellpose.org/)**  
- **[Cellpose Google Colab](https://colab.research.google.com/github/MouseLand/cellpose/blob/main/notebooks/Cellpose_cell_segmentation_2D_prediction_only.ipynb)**  

---

#### Instalación de Anaconda
##### **Paso 1: Descargar e instalar Anaconda**

1. Descarga el instalador desde:  
   [**Anaconda para Windows**](https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Windows-x86_64.exe)  
   ![Instalador de Anaconda](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/imagenAnaconda1.png)

2. Ejecuta el instalador y sigue estos pasos:
   
   - Da clic en continuar "Next".
   - Acepta los términos y condiciones.
   - Instala Anaconda en una cuenta local para evitar conflictos futuros y da clic en siguiente.
     ![Instalación en cuenta local](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/justme.png)
   - Configura Anaconda como el programa predeterminado para ejecutar Python. Solo selecciona la tercer casilla.
     
3. Haz clic en **Install** para iniciar la instalación.  
   ![Botón instalación](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/installAnaconda.png)

##### **Paso 2: Crear un ambiente en Anaconda**

Los entornos de Conda permiten gestionar paquetes y sus dependencias de manera aislada, evitando conflictos entre proyectos.

1. Ve a la sección de **Environments**.  
2. Haz clic en **Create**.  
3. Configura el ambiente:
   
   - **Name**: TallerMultiplex-IA  
   - **Python version**: 3.12.7
   - 
4. Haz clic en **Create**.
   ![Crear ambiente](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/crearAmbienteAnaconda.png)
5. Una vez creado, el ambiente estará disponible en la lista de entornos. Para seleccionarlo, simplemente haz clic en él.

---

#### Instalación de Cellpose

##### **Paso 1: Instalar Cellpose en el ambiente creado**

1. Selecciona el ambiente **TallerMultiplex-IA** en la lista de entornos.
2. Haz clic en **Open terminal**.  
   ![Iniciar ambiente](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/iniciarTerminalAmbiente.png)
   
4. En la terminal, escribe el siguiente comando y presiona Enter:  
   ```bash
   python -m pip install cellpose[gui]
   ```
5. Una vez completada la instalación, debería verse un mensaje confirmando la instalación exitosa.
 ![Desarrollo instalacion Cellpose](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/instalacionCellpose.png)

##### **Paso 2: Ejecutar Cellpose**

1. Desde la terminal del ambiente, ejecuta el comando:
   ```bash
   python -m cellpose
   ```
![Vista instalacion Cellpose](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/comandoAbrirCellpose.png)

2. Esto abrirá la interfaz gráfica (GUI) de Cellpose lista para usarse.
![Vista Cellpose](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/vistaCellposeGUI.png)

![Cellpose parámetros](/202411_LNMA_IA-mIF/assets/Imagenes/GuiaAnacondaCellpose/cellpose_gui.png)

