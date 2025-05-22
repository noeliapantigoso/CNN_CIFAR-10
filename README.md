# 🧠 Clasificación de Imágenes con CNN – CIFAR-10  
**Trabajo Final DMC – Especialización en Machine Learning & Deep Learning**

---

## 📌 Descripción del proyecto

Este proyecto implementa una Red Neuronal Convolucional (CNN) para la clasificación de imágenes en el conjunto de datos **CIFAR-10**, que contiene 10 categorías visuales:
avión, automóvil, pájaro, gato, ciervo, perro, rana, caballo, barco, camión


---

## 📁 Dataset

- 60,000 imágenes (32x32 px, RGB)
- 50,000 para entrenamiento / 10,000 para test
- Enlace: [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)

---

## 🏗️ Arquitectura del modelo

- Capas `Conv2D` + `ReLU`
- `MaxPooling2D` y `Dropout`
- `Flatten` → `Dense(128)` → `Dense(10)`
- Optimización: `SGD` con `learning_rate=0.001`, `momentum=0.9`
- Función de pérdida: `categorical_crossentropy`

---

## 📈 Resultados

- Accuracy final sobre test: **71.5%**
- Overfitting identificado a partir de la época **70**
- Modelo guardado como `modelo_final.h5`

---

## 🧪 Predicción personalizada

```bash
python predict_image.py gato.png
python predict_image.py barco.png


Imágenes predichas correctamente con clases esperadas:

[3] → gato
[8] → barco


