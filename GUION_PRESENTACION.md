# GUION PRESENTACIÓN - OPTIMIZACIÓN CON PROGRAMACIÓN LINEAL
## Grupo 2: Dante Passone & Braian Tormey

---

## APERTURA

- Presentamos dos ejercicios de optimización usando programación lineal y Python.
- El objetivo es mostrar cómo resolver problemas reales maximizando beneficios bajo restricciones.

---

## EJERCICIO 2: PAQUETES ESCOLARES

### Portada
- Mostramos el título: "Paquetes Escolares" y el número de ejercicio.
- El subtítulo indica que vamos a maximizar el beneficio de los paquetes.
- Los íconos representan los recursos: cuadernos, carpetas, bolígrafos y el beneficio.

### Enunciado
- Se explica el problema: hay que armar paquetes escolares usando el stock disponible.
- Hay dos tipos de paquetes, cada uno con distinta composición y precio.
- El objetivo es decidir cuántos paquetes de cada tipo fabricar para ganar lo máximo posible.

### Datos y Stock
- Se muestra el stock disponible: 600 cuadernos, 500 carpetas, 400 bolígrafos.
- El objetivo es maximizar la ganancia respetando estos límites.

### Restricciones
- Se presentan las restricciones:
  - Cuadernos: 2x + 3y ≤ 600
  - Carpetas: x + y ≤ 500
  - Bolígrafos: 2x + y ≤ 400
  - No negatividad: x ≥ 0, y ≥ 0
- Cada restricción asegura que no se use más stock del disponible.

### Región factible
- La región factible es el área de solución: todas las combinaciones posibles de paquetes que cumplen todas las restricciones.
- En el gráfico, es el área sombreada o polígono donde se pueden encontrar soluciones válidas.

### Implementación en Python
- Se explica que usamos Python y la librería PuLP para modelar el problema.
- Paso a paso:
  - Se instala PuLP.
  - Se importan las librerías.
  - Se crea el problema de maximización.
  - Se definen las variables de decisión: x (paquetes tipo 1), y (paquetes tipo 2).
  - Se define la función objetivo: 6.5x + 7y.
  - Se agregan las restricciones.
  - Se resuelve el problema con el solver.
  - Se muestran los resultados: cuántos paquetes de cada tipo fabricar y la ganancia máxima.

### Resultados y Gráfico
- Se muestra la solución óptima: 150 paquetes tipo 1 y 100 paquetes tipo 2, ganancia total 1.675 euros.
- El gráfico muestra la región factible y la solución óptima.
- Aclarar: la solución óptima ocurre cuando la función objetivo (la línea de ganancia máxima) pasa por uno de los vértices del área de solución.
- Es decir, siempre que maximizamos, la mejor solución está en un vértice de la región factible.

---

## ACLARACIONES CLAVE
- Región factible = área de solución: todas las combinaciones posibles que cumplen las restricciones.
- Solución óptima: ocurre en un vértice de la región factible, donde la función objetivo es máxima.

---

## ANÁLISIS DE MEJORAS - PAQUETES ESCOLARES (3 minutos)

El análisis de sensibilidad nos permite evaluar el impacto de cambios en los parámetros del problema. Consideramos dos escenarios de mejora.

En el primer escenario, aumentamos el stock de bolígrafos de 400 a 450 unidades. Este cambio permite fabricar más paquetes tipo 1, que son más rentables por unidad. El resultado muestra un incremento en la ganancia total.

En el segundo escenario, reducimos el stock de carpetas de 500 a 250 unidades. Este análisis revela que las carpetas tienen un exceso significativo, por lo que esta reducción no afecta la ganancia pero sí reduce costos de almacenamiento y capital inmovilizado.

Estos análisis demuestran el valor de la programación lineal no solo para encontrar soluciones óptimas, sino también para evaluar la robustez de estas soluciones ante cambios en las condiciones del problema.

---

## PROBLEMA 2: JOYAS ARTESANALES (12 minutos)

### Enunciado (2 minutos)

Nuestro segundo caso de estudio aborda un problema de manufactura artesanal completamente diferente. Un orfebre debe optimizar la producción de joyas considerando limitaciones de metales preciosos.

Este problema es representativo de industrias donde los recursos son costosos y escasos, y donde la optimización puede tener un impacto significativo en la rentabilidad del negocio.

El orfebre dispone de 750 gramos de oro y 750 gramos de plata, y puede fabricar dos tipos de joyas con diferentes composiciones y precios de venta.

### Modelo Matemático (3 minutos)

El modelo matemático para este problema es más simétrico que el anterior. Definimos x como la cantidad de joyas tipo A e y como la cantidad de joyas tipo B.

La función objetivo 40x + 50y representa el beneficio total, donde cada coeficiente corresponde al precio de venta de cada tipo de joya.

Las restricciones reflejan el consumo de metales preciosos. Para el oro: x + 1.5y ≤ 750, donde la joya tipo A consume 1 gramo y la tipo B consume 1.5 gramos.

Para la plata: 1.5x + y ≤ 750, donde la joya tipo A consume 1.5 gramos y la tipo B consume 1 gramo. Esta simetría en las restricciones es matemáticamente interesante y nos llevará a una solución equilibrada.

Las restricciones de no negatividad x ≥ 0, y ≥ 0 son igualmente importantes en este contexto.

### Implementación en Python (4 minutos)

La implementación en Python sigue la misma metodología, pero ahora trabajamos con un problema donde ambas restricciones son igualmente importantes.

Creamos un nuevo objeto LpProblem llamado 'Problema_Joyas' y definimos nuestras variables de decisión con las mismas especificaciones de enteros y no negatividad.

La función objetivo 40*x + 50*y se define de manera similar. Las restricciones se implementan usando las ecuaciones matemáticas que derivamos del análisis del problema.

El método solve() ejecuta el algoritmo de optimización. En este caso, el problema es más equilibrado, lo que se reflejará en la solución final.

### Resultados y Análisis (3 minutos)

La solución óptima es: 300 joyas tipo A y 300 joyas tipo B, generando un beneficio total de 27.000 euros.

Esta solución es matemáticamente elegante porque ambas restricciones son activas simultáneamente. Esto significa que tanto el oro como la plata se consumen completamente, sin excesos.

El gráfico muestra que la solución óptima se encuentra en la intersección de las dos restricciones principales. Esta propiedad matemática es fundamental: cuando dos restricciones son activas, la solución se encuentra en su punto de intersección.

La simetría de la solución (300 de cada tipo) refleja la simetría en las restricciones del problema. Este es un ejemplo clásico de cómo la estructura matemática del problema se refleja en la estructura de la solución.

---

## ANÁLISIS DE MEJORAS - JOYAS (3 minutos)

El análisis de mejoras para este problema es diferente al anterior. Como no hay excesos de recursos, las mejoras deben venir de aumentar la disponibilidad de materiales.

Consideramos el escenario de aumentar el stock a 900 gramos de oro y 900 gramos de plata. Este cambio permite fabricar 360 joyas de cada tipo, aumentando el beneficio total a 32.400 euros.

Este análisis demuestra el concepto de rendimientos marginales decrecientes: el incremento en el beneficio no es proporcional al incremento en los recursos, debido a las restricciones lineales del problema.

La visualización muestra cómo la región factible se expande, pero mantiene su forma geométrica fundamental, lo cual es una propiedad importante de la programación lineal.

---

## CONCLUSIONES Y REFLEXIONES FINALES (3 minutos)

Hemos demostrado exitosamente cómo la programación lineal puede aplicarse a problemas empresariales muy diferentes, desde logística educativa hasta manufactura artesanal.

Los dos problemas ilustran conceptos fundamentales: el primero muestra un problema con recursos desequilibrados donde una restricción es claramente limitante, mientras que el segundo muestra un problema equilibrado donde múltiples restricciones son activas simultáneamente.

Python con PuLP demostraron ser herramientas excepcionalmente poderosas para implementar estos modelos. La combinación de simplicidad de uso y robustez matemática hace de esta tecnología una opción ideal para optimización empresarial.

Los análisis de sensibilidad que realizamos son cruciales en la práctica empresarial, ya que permiten evaluar la robustez de las soluciones e identificar oportunidades de mejora.

La programación lineal sigue siendo una de las herramientas más importantes en investigación operativa, con aplicaciones en logística, finanzas, manufactura, y muchos otros campos.

---

## CIERRE (1 minuto)

En conclusión, hemos demostrado que la programación lineal, implementada con Python y PuLP, puede transformar problemas empresariales complejos en soluciones óptimas y cuantificables.

La metodología que hemos presentado es aplicable a una amplia gama de problemas reales, y las herramientas que hemos utilizado están disponibles gratuitamente, democratizando el acceso a técnicas avanzadas de optimización.

Gracias por su atención. ¿Hay alguna pregunta sobre nuestro trabajo o sobre las aplicaciones de la programación lineal en otros contextos?

---

## PUNTOS CLAVE PARA DESTACAR

1. **Dominio técnico:** Conocimiento profundo de algoritmos de optimización
2. **Análisis crítico:** Identificación de restricciones activas y oportunidades de mejora
3. **Aplicabilidad práctica:** Conexión clara entre teoría matemática y problemas reales
4. **Metodología sistemática:** Enfoque estructurado desde modelado hasta implementación
5. **Pensamiento analítico:** Capacidad de interpretar resultados y extraer insights
6. **Comunicación técnica:** Explicación clara de conceptos complejos

**¡PRESENTACIÓN COMPLETA Y PROFESIONAL! 🚀**

---

## POSIBLES PREGUNTAS Y RESPUESTAS RÁPIDAS

**¿Qué es la región factible?**
- Es el área donde se cumplen todas las restricciones.

**¿Por qué la solución óptima está en un vértice?**
- Porque en programación lineal, el máximo o mínimo siempre se da en un vértice del área de solución.

**¿Qué pasa si cambio el stock de un recurso?**
- Puede cambiar la solución óptima y la ganancia máxima.

**¿Por qué usamos variables enteras?**
- Porque no se pueden fabricar fracciones de paquetes o joyas.

**¿Qué hace PuLP?**
- Resuelve problemas de optimización lineal de forma automática.

**¿Qué significa una restricción activa?**
- Es la que se cumple como igualdad en la solución óptima, limita el resultado.

**¿Qué es la función objetivo?**
- Es la fórmula que queremos maximizar o minimizar (la ganancia total).

**¿Qué pasa si hay más de un vértice óptimo?**
- Hay varias soluciones óptimas, todas dan el mismo valor máximo.

**¿Qué representa el gráfico?**
- Muestra el área de soluciones posibles y el punto óptimo.

**¿Por qué hay recursos que sobran?**
- Porque no siempre todos los recursos se usan al máximo en la solución óptima.

**¿Se puede usar este método para otros problemas?**
- Sí, sirve para cualquier problema con restricciones y objetivo lineal.

**¿Qué pasa si una restricción no se cumple?**
- La solución no es válida, debe estar dentro del área de solución.

**¿Por qué es importante la no negatividad?**
- Porque no se pueden fabricar cantidades negativas.

**¿Qué significa sensibilidad o análisis de mejoras?**
- Ver cómo cambian los resultados si cambian los datos del problema.

**¿Por qué usamos Python?**
- Porque es fácil, rápido y tiene librerías como PuLP para optimización.

**¿Qué significa maximizar y minimizar en programación lineal?**
- Maximizar es buscar el mayor valor posible de la función objetivo; minimizar es buscar el menor.

**¿Qué pasa si no hay solución factible?**
- El modelo no tiene ninguna combinación que cumpla todas las restricciones.

**¿Qué es una variable de decisión?**
- Es lo que queremos calcular, por ejemplo, cuántos paquetes o joyas fabricar.

**¿Qué es una restricción redundante?**
- Es una restricción que no afecta la región factible porque ya está cubierta por otras.

**¿Qué pasa si cambio el precio de venta?**
- Puede cambiar la función objetivo y la solución óptima.

**¿Por qué a veces la solución óptima no usa todo el stock?**
- Porque otra restricción se vuelve limitante antes de agotar todos los recursos.

**¿Qué significa 'entero' en las variables?**
- Que solo se permiten valores sin decimales (no fraccionarios).

**¿Qué hago si el solver da un resultado decimal y necesito enteros?**
- Se debe usar variables de tipo entero en el modelo.

**¿Qué es el método simplex?**
- Es un algoritmo que encuentra la solución óptima en programación lineal.

**¿Qué errores comunes hay al modelar?**
- Plantear mal las restricciones, olvidar la no negatividad, o no definir bien la función objetivo.

**¿Cómo interpreto el gráfico si hay más de dos variables?**
- No se puede graficar fácilmente, pero el método sigue siendo válido.

**¿Qué significa que una variable valga cero en la solución?**
- Que no conviene fabricar ese tipo de producto en la solución óptima.

**¿Qué pasa si todas las restricciones son inactivas?**
- No es posible, siempre al menos una es activa en la solución óptima.

**¿Por qué a veces hay varias soluciones óptimas?**
- Porque la función objetivo es paralela a una arista de la región factible.

**¿Qué es el análisis de sensibilidad?**
- Es ver cómo cambian los resultados si cambian los datos del problema.

**¿Qué pasa si cambio una restricción por un valor menor?**
- La región factible se achica y puede cambiar la solución óptima.

**¿Qué significa 'solver'?**
- Es el programa que resuelve el modelo matemático.

**¿Por qué usamos PuLP y no Excel?**
- PuLP es más flexible, permite automatizar y manejar problemas más grandes.

**¿Qué hago si el modelo tarda mucho en resolver?**
- Revisar si el problema es muy grande o si hay errores en la formulación.

**¿Se puede usar para problemas de minimización de costos?**
- Sí, solo hay que cambiar la función objetivo a minimizar.

**¿Qué significa 'no acotado'?**
- Que la función objetivo puede crecer indefinidamente, falta alguna restricción.

**¿Qué hago si el resultado no tiene sentido práctico?**
- Revisar el modelo, los datos y las restricciones.

**¿Qué es una solución factible?**
- Es cualquier combinación de variables que cumple todas las restricciones.

**¿Por qué es importante interpretar los resultados?**
- Para tomar decisiones correctas y entender el impacto de cada restricción.

**¿Qué pasa si cambio el tipo de variable a continua?**
- El solver puede dar soluciones con decimales, útiles en otros contextos.

**¿Qué es una función lineal?**
- Es una función donde las variables solo aparecen multiplicadas por constantes y sumadas.

**¿Por qué la programación lineal es útil en empresas?**
- Permite optimizar recursos y maximizar ganancias o minimizar costos de forma sistemática.

**¿Se puede usar para planificar horarios o rutas?**
- Sí, siempre que el problema se pueda expresar con restricciones y objetivo lineal.

**¿Qué hago si el modelo no refleja la realidad?**
- Ajustar las restricciones o la función objetivo para que representen mejor el problema real.

**¡PRESENTACIÓN COMPLETA Y PROFESIONAL! 🚀** 