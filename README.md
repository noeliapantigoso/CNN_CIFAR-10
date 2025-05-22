🧠 Clasificación de Imágenes con CNN – CIFAR-10
Trabajo Final DMC – Especialización en Machine Learning & Deep Learning

📌 Descripción del proyecto
Este proyecto implementa una Red Neuronal Convolucional (CNN) para la clasificación de imágenes en el conjunto de datos CIFAR-10, que contiene 10 categorías visuales: avión, automóvil, pájaro, gato, ciervo, perro, rana, caballo, barco y camión.

Se utilizó un modelo inspirado en la arquitectura VGG, con técnicas como Dropout, normalización de pixeles y entrenamiento con SGD, logrando una precisión de ~71.5% sobre el conjunto de validación.

🖼️ Dataset
📦 60,000 imágenes en total (32x32 px, RGB).

50,000 imágenes para entrenamiento.

10,000 imágenes para testeo.

✅ 10 clases balanceadas (5,000 imágenes por clase en entrenamiento).

📥 Dataset oficial: CIFAR-10

🏗️ Estructura del modelo
🔷 2 capas Conv2D con filtros 3x3 y activación ReLU.

🔷 MaxPooling2D y Dropout para reducir overfitting.

🔷 Flatten seguido de capa Dense con 128 neuronas.

🔷 Salida con softmax sobre 10 clases.

🔧 Optimización con SGD (LR = 0.001, momentum = 0.9).

🔁 Flujo del proyecto
Carga y visualización de datos

One-hot encoding de etiquetas

Normalización de pixeles

Definición del modelo CNN

Entrenamiento (100 épocas)

Evaluación del modelo

Predicción personalizada de imágenes externas

Guardado del modelo en .h5

📈 Resultados
Precisión final sobre test: 71.5%

Se detectó overfitting a partir de la época 70, sugerencia: detener el entrenamiento antes o usar técnicas como aumento de datos (data augmentation).

📦 Ejecución del modelo
bash
Copiar
Editar
# Entrenamiento
python train_model.py

# Predicciones (requiere 'modelo_final.h5' entrenado)
python predict_image.py barco.png
📁 Archivos importantes
modelo_final.h5: Modelo entrenado y serializado.

train_model.py: Entrena la CNN desde cero.

predict_image.py: Carga una imagen 32x32 y predice su clase.

barco.png, gato.png, carro.png: Imágenes de prueba externas.

🧪 Ejemplo de predicciones
bash
Copiar
Editar
[8]  # barco
[3]  # gato
[1]  # automóvil
🧠 Autor
Trabajo desarrollado en el marco de la Especialización DMC – Machine Learning y Deep Learning (CNN).

✅ Para subir a GitHub:
Asegúrate de tener tu carpeta así:

objectivec
Copiar
Editar
CIFAR10_CNN/
├── train_model.py
├── predict_image.py
├── modelo_final.h5
├── gato.png
├── barco.png
├── carro.png
├── README.md
Subida al repositorio:

bash
Copiar
Editar
cd CIFAR10_CNN
git init
git add .
git commit -m "Proyecto CNN CIFAR-10 final"
git remote add origin https://github.com/tuusuario/CIFAR10_CNN.git
git push -u origin master
