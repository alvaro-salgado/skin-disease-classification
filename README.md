# 🧠 Clasificación de Lesiones Cutáneas mediante Redes Neuronales Convolucionales

Este proyecto implementa una **Red Neuronal Convolucional (CNN)** para la **clasificación automática de lesiones cutáneas** utilizando el conjunto de datos **ISIC 2018**, con el objetivo de apoyar el diagnóstico temprano de enfermedades dermatológicas mediante técnicas de *Deep Learning*.

---

## 📊 Conjunto de Datos

- **Fuente:** [ISIC 2018 Challenge Dataset](https://challenge.isic-archive.com/data/)
- **Total de imágenes:** 10,015
- **Tipo de datos:** Imágenes etiquetadas de diversas lesiones cutáneas
- **Propósito:** Entrenamiento, validación y evaluación del modelo

---

## 🧩 Preprocesamiento de Imágenes

Se realizaron las siguientes etapas de preparación de datos:

- 🔹 **Redimensionado:** Adaptación de las imágenes a un tamaño uniforme  
- 🔹 **Normalización:** Escalado de valores de píxeles entre 0 y 1  
- 🔹 **Aumento de Datos (Data Augmentation):** Rotaciones, volteos, zoom y desplazamientos aleatorios  
- 🔹 **Sobremuestreo de Clases:** Incremento sintético de muestras minoritarias para reducir el desbalance de clases  

---

## 🏗️ Arquitectura del Modelo CNN

| Parámetro | Descripción |
|------------|-------------|
| **Capas convolucionales** | 3 (con 16, 32 y 64 filtros) |
| **Tamaño del kernel** | 3x3 |
| **Capas densas** | 512, 64 y 32 unidades |
| **Dropout** | 50% y 30% en las capas densas |
| **Funciones de activación** | ReLU (ocultas) y Softmax (salida) |

---

## 📈 Resultados del Modelo

| Métrica | Valor |
|----------|--------|
| **Exactitud (Accuracy)** | 63.76% |
| **Precisión** | 70.21% |
| **Recall** | 63.76% |
| **F1-Score (Macro)** | 65.72% |
| **AUC (Área bajo la curva ROC)** | 82.1% |

---

## 🧠 Análisis de Desempeño

El modelo demuestra un desempeño competitivo en la **clasificación de lesiones cutáneas**, logrando una buena **capacidad de discriminación (AUC: 82.1%)** y una **precisión razonable (70.21%)**.  
Sin embargo, las **clases minoritarias** aún presentan desafíos, evidenciando la necesidad de estrategias adicionales como:

- Balanceo avanzado de clases (SMOTE, focal loss, etc.)  
- Arquitecturas más profundas o preentrenadas (p. ej. ResNet, EfficientNet)  
- Ajuste de hiperparámetros y regularización adicional  

---

## ⚙️ Tecnologías Utilizadas

- Python 3.x  
- TensorFlow / Keras  
- NumPy, Pandas, Matplotlib  
- Scikit-learn  

---

## 📚 Créditos

**Autor:** Álvaro Salgado  
**Curso:** Deep Learning — Proyecto Final  
**Institución:** Universidad Autónoma de Nuevo León (UANL)  
**Dataset:** ISIC 2018 Challenge Dataset  

---

## 🩺 Conclusión

El modelo propuesto constituye un paso importante hacia la **automatización del diagnóstico dermatológico**, mostrando potencial para asistir en la detección de lesiones cutáneas mediante *Deep Learning*.  
A futuro, se planea implementar **modelos preentrenados** y **técnicas de interpretación visual** (Grad-CAM) para mejorar la precisión y la transparencia del sistema.
