# Apuntes de Métodos Numéricos en Java

Este repositorio reúne apuntes teóricos y ejemplos prácticos sobre métodos numéricos aplicados mediante el lenguaje de programación Java. Está orientado a estudiantes de ingeniería y ciencias computacionales que buscan comprender y aplicar técnicas de análisis numérico en problemas reales.

## 1. Interpolación

### ¿Qué es la interpolación?

La interpolación es un método que permite estimar valores intermedios entre puntos conocidos de una función. Se utiliza comúnmente cuando se cuenta con una tabla de datos discretos y se desea predecir el comportamiento de la función entre dichos puntos.

### Tipos de interpolación

#### Interpolación lineal

- Método más simple.
- Supone que los datos entre dos puntos conocidos siguen una línea recta.
- Adecuado cuando los puntos están cercanos y la función varía de forma casi lineal.

Fórmula:

    y = y0 + ( (y1 - y0) / (x1 - x0) ) * (x - x0)

#### Interpolación polinómica (método de Newton)

- Usa polinomios de orden superior para ajustar varios puntos.
- Basado en diferencias divididas.
- Permite agregar nuevos puntos sin recalcular todo el polinomio.
- Puede producir oscilaciones si se usan muchos puntos.

## 2. Regresión y correlación

### ¿Qué es la regresión?

La regresión se utiliza para encontrar una función que represente la tendencia general de un conjunto de datos. A diferencia de la interpolación, no requiere que la función pase exactamente por todos los puntos.

### ¿Qué es la correlación?

La correlación mide la fuerza y dirección de la relación lineal entre dos variables. Se expresa mediante un coeficiente r:

- r > 0: correlación positiva
- r < 0: correlación negativa
- r = 0: no hay correlación lineal

### Regresión lineal

- Modelo matemático: y = a + bx
- Se determinan los coeficientes a (intersección) y b (pendiente) usando fórmulas de mínimos cuadrados.
- Se aplica ampliamente en ingeniería, economía y ciencia de datos.

## 3. Método de mínimos cuadrados

### ¿Qué es?

El método de mínimos cuadrados busca una curva que minimice la suma de los errores cuadrados entre los valores reales y los estimados por el modelo. Es especialmente útil cuando los datos contienen errores o ruido.

Aplicaciones comunes:

- Ajuste lineal o cuadrático de datos experimentales.
- Predicción basada en tendencias observadas.

Ventajas:

- No requiere que la curva pase por todos los puntos.
- Fácil de implementar computacionalmente.

Limitaciones:

- El modelo debe ser adecuado para los datos (por ejemplo, usar regresión lineal con datos no lineales puede llevar a errores importantes).

## 4. Otros métodos numéricos importantes

Aunque no todos se desarrollan en este repositorio, es útil conocer otros métodos fundamentales en análisis numérico:

### Método de la bisección

- Encuentra raíces de ecuaciones f(x) = 0.
- Requiere un intervalo [a, b] donde f(a) * f(b) < 0.
- Divide el intervalo a la mitad iterativamente hasta alcanzar la precisión deseada.
- Es lento pero seguro.

### Método de Newton-Raphson

- Método iterativo para encontrar raíces.
- Usa derivadas: x_{n+1} = x_n - f(x_n) / f'(x_n)
- Requiere una buena estimación inicial y que f'(x) ≠ 0.
- Converge rápidamente, pero puede fallar si la función es complicada.

## 5. Aplicaciones de los métodos numéricos

Estos métodos se utilizan en diversas disciplinas:

- Ingeniería: análisis de sistemas físicos, estimaciones experimentales.
- Ciencias aplicadas: simulaciones, ajustes de modelos.
- Economía: proyecciones, análisis de tendencias.
- Ciencia de datos: entrenamiento de modelos, predicción de variables.
- Meteorología, biología, química computacional, entre otros.



## Bibliografía 
- Chapra, S. C., & Canale, R. P. (2006). *Métodos numéricos para ingenieros*.
- Burden, R. L., & Faires, J. D. (2011). *Análisis numérico*.
