# The Deep Learning Archive (El archivo de Deep Learning)
[Read in English](../README.md) | [Leer en Español](README.md)

> Exploraciones teóricas y rigurosas del núcleo de las arquitecturas de Deep Learning, desglosadas paso a paso.

---

## Introducción

¿Alguna vez te has preguntado por qué, al construir una red neuronal, no podemos simplemente inicializar todos los pesos en 1, o en 0, o incluso en valores aleatorios gigantes como punto de partida? Porque, bueno, al final, se van a ir afinando solos a través del entrenamiento, ¿no?

Seguramente has escuchado mucho de los problemas de "desvanecimiento de gradientes" (*Vanishing Gradients*) o "gradientes que explotan" (*Exploding Gradients*) que causan que tu red "muera" rápidamente: los gradientes desaparecen o las neuronas se saturan, dejando a la red incapaz de aprender incluso el patrón más simple.

Este espacio no es solo una colección de resúmenes teóricos; es un archivo de derivaciones desde cero. Mi objetivo es acompañarte a través de estas páginas de razonamiento lógico, matemático y estadístico que llevaron a los grandes avances del Deep Learning. No aceptaremos ninguna "fórmula" como caída del cielo; construiremos cada una de ellas usando las herramientas fundamentales de la matemática.

---

## Artículos Publicados

### Fundamentos de Deep Learning
* 🧠 **Por Qué Mueren las Redes Neuronales: La Matemática Detrás del Vanishing Gradient Problem:**
  Un análisis profundo del flujo de datos a través de un Perceptrón Multicapa (MLP). Este artículo abre la caja negra del cálculo multivariable y la regla de la cadena total durante el *backward pass* para demostrar matemáticamente el origen exacto donde colapsan los gradientes.
  * [Leer Artículo (ES)](https://bastianru.github.io/deep-learning-archive/es/why-nn-die/P1)
  * [Read Article (EN)](https://bastianru.github.io/deep-learning-archive/en/why-nn-die/P1)

* 🧪 **La Matemática Detrás de la Inicialización de Xavier (Próximamente):**
  Como una continuacion directa del primer articulo, partiendo del problema de la degradación del gradiente, derivaremos matemáticamente los factores exactos de escalado de varianza propuestos por Xavier Glorot y Yoshua Bengio en 2010 para mantener las señales vivas a lo largo de arquitecturas profundas.

---

## ¿Es esto para ti? (Prerrequisitos)

Estos artículos están diseñados para ser lo más accesibles posible. Sin embargo, para seguir el hilo de las demostraciones sin perderte, es recomendable contar con los siguientes conocimientos previos mínimos:

**Para el análisis del forward pass y estadística:**
- **Arquitectura MLP:** Entender neuronas, capas y sus conexiones (el producto punto fundamental $z = Wx + b$).
- **Estadística Descriptiva:** Sentirse cómodo con los conceptos de Media ($\mu$) y Varianza ($\sigma^2$) / Desviación Estándar.
- **Álgebra Básica:** Resolución de ecuaciones, potencias y raíces cuadradas.

**Para el análisis del backward pass y optimización:**
- **Cálculo Diferencial:** Comprender qué representa una derivada.
- **Derivadas Parciales:** Entender cómo derivar con respecto a una variable manteniendo las demás constantes.
- **Backpropagation Básico:** Una noción conceptual de cómo fluye el error hacia atrás en una red.

Si cumples con estos requisitos, construiremos el resto aquí. Cada propiedad estadística avanzada o truco matemático se definirá formalmente justo antes de que lo necesitemos para el siguiente paso de la demostración.