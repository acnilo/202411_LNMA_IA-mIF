---
title: Creación de proyectos en QuPath
date: 2024-10-25
categories:
- Qupath
excerpt: |
  Creación de proyecto en QuPath
feature_text: |
  ##  Proyectos en QuPath  
---
### ¿Qué es un proyecto en QuPath?
QuPath permite ver y trabajar con imágenes individuales, pero si planeas guardar y recargar datos asociados con varias imágenes, se recomienda usar un proyecto.
<ul>
    <li>Agrupar imágenes relacionadas</li>
    <li>Cambiar fácilmente entre imágenes (haciendo clic en miniaturas en la lista de imágenes del proyecto)</li>
    <li>Organizar tus archivos de datos junto con scripts, clasificadores y otros elementos útiles</li>
    <li>Ver una miniatura más grande y algunos datos del archivo al pasar el ratón sobre una imagen, sin tener que abrirla por completo</li>
</ul>
---

### Crear un proyecto en QuPath

**1. Crear una carpeta de proyecto**

1.1. Crea una carpeta vacía en tu computadora.
1.2. Configúrala como carpeta del proyecto mediante una de las siguientes opciones:
  - **Archivo** ‣ Proyecto… ‣ Crear nuevo proyecto.
  - **Arrastrar y soltar**: Arrastra la carpeta y suéltala sobre QuPath.  

**Nota:**  
La carpeta debe estar vacía, ya que QuPath gestionará su contenido. No añadas, elimines ni renombres archivos manualmente.

**2. Agregar imágenes al proyecto**

- Arrastra las imágenes hacia la ventana de QuPath.  
- Configura las opciones de importación en el diálogo que aparecerá.  

{% include video.html id="kCEp89ypmAY" title="Tutorial creación de proyecto en QuPath" %}

---

### Introducción a los objetos en QuPath

**Tipos de objetos:**

- **Anotaciones:** Dibujadas manualmente sobre la imagen.  
- **Detecciones:** Generadas automáticamente, por ejemplo, células individuales.

**Diferencias clave:**

- **Anotaciones**: Pocas y abarcan áreas grandes.  
- **Detecciones**: Pueden ser millones, manejadas eficientemente por QuPath.

**Dibujar anotaciones**

1. Selecciona la herramienta de dibujo (Rectángulo, Elipse, Polígono o Pincel).  
2. Haz clic y arrastra sobre la imagen.  
3. Explora herramientas adicionales:
   - Polígono: Haz clic en cada vértice; finaliza con doble clic.
{% include video.html id="FAoUHu40dk0" title="Introducción a los objetos en QuPath" %}
---

### Conteo manual de células

**Elegir una región**

Selecciona un área adecuada en la imagen. Para mayor precisión, usa la herramienta de cuadrícula.

1. Selecciona la herramienta de punto.  
2. Haz clic en la imagen para crear un punto por célula.  
3. Cambia categorías de puntos en el panel de conteo.  

{% include video.html id="L-dLnkqHKdY" title="Conteo de células" %}

---

### Detección automática de células

1. Crea una anotación en un área pequeña (aprox. 100 células).  
2. Ejecuta **Analizar ‣ Detección de células ‣ Detección de células**.  
3. Ajusta los parámetros o utiliza los predeterminados.  
4. Presiona **Ejecutar** para generar las detecciones.

---

### Generar tablas de medición

1. Haz clic en el botón **Tabla** en la barra de herramientas.  
2. Selecciona el tipo de objetos (anotaciones o detecciones).  
3. Exporta los datos como CSV o copia para otras aplicaciones como Excel.  

{% include video.html id="9P8NsAVfrZE" title="Generación de tablas" %}

---

### Detección de tejido con umbrales (threshold)

1. Usa **Clasificar ‣ Clasificación de píxeles ‣ Crear umbral** para destacar regiones específicas.  
2. Haz clic en **Crear objetos** para generar anotaciones basadas en el umbral.  

{% include video.html id="9TmEb3SxS1k" title="Generación de tablas" %}

---

### Integración de Cellpose/Omnipose en QuPath

**Paso 1: Instalar Cellpose/Omnipose**

1. Configura un entorno virtual de Python.  
2. Instala Cellpose y/o Omnipose siguiendo las guías en sus repositorios:  
   - [Cellpose](https://github.com/MouseLand/cellpose)  
   - [Omnipose](https://github.com/masenf/omnipose)  
3. Añade `scikit-image` como dependencia:  
   - Con `pip`: `python -m pip install scikit-image`.  
   - Con `conda`: `conda install scikit-image`.

**Paso 2: Configurar la extensión de Cellpose en QuPath**

1. Descarga el archivo `qupath-extension-cellpose-[version].zip`.  
2. Instálalo arrastrando el `.jar` a la ventana principal de QuPath.  
3. Configura las preferencias en **Editar > Preferencias > Cellpose/Omnipose**:  
   - Proporciona las rutas de los ejecutables de Python para Cellpose y Omnipose.

{% include video.html id="A_PW_N0np9A" title="Cellpose/Omnipose en QuPath" %}
