# 🍩 Sistema inteligente para control de cocción de donas

**Autor:** Edwin Gabriel Naranjo Velastegui  
**Maestría en Inteligencia Artificial Aplicada - UDLA**

## 📌 Descripción del problema y solución

En la panadería *Micro Quito y Panadería* la evaluación del punto de cocción de las donas se realiza visualmente, generando variabilidad y desperdicio. Este proyecto desarrolla un sistema de clasificación basado en visión artificial (Teachable Machine) que distingue tres niveles de cocción: **insuficiente, óptima, sobrecocción**.

El modelo alcanza **100% de precisión** en condiciones controladas.

## 🚀 Instrucciones de uso

1. Abrir: [https://teachablemachine.withgoogle.com/models/cvY-3tZmk/](https://teachablemachine.withgoogle.com/models/cvY-3tZmk/)
2. Conceder permisos de cámara.
3. Colocar una dona frente a la cámara (fondo oscuro, luz fija, distancia ~30 cm).
4. Leer la clasificación y confianza.
5. Si la confianza es inferior al 95%, repetir la captura.

## 📊 Resultados

- Precisión global: 100% (141 imágenes de prueba)
- Matriz de confusión: diagonal perfecta
- Sensibilidad: la clase óptima falla con brillo >20% o rotación >15°

## 📂 Estructura del repositorio
CAPSTONE-MIA/
├── README.md
├── docs/ (documentos del proyecto)
├── modelo/ (archivos .tm del modelo)
├── data/ (imágenes del dataset por clase)
├── pruebas_robustez/ (oclusiones y stress-tests)

## 🔗 Enlace al prototipo

[https://teachablemachine.withgoogle.com/models/cvY-3tZmk/](https://teachablemachine.withgoogle.com/models/cvY-3tZmk/)

## ⚠️ Limitaciones

- Solo válido para donas sin glaseado, con iluminación estandarizada.
- No usar con luz natural variable.
- Requiere fondo oscuro y distancia fija.

## 📝 Trabajo futuro

- Aumentar dataset con variaciones de brillo y rotación.
- Implementar control de lux con el móvil.
