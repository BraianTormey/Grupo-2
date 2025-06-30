# GUION PRESENTACIÓN - OPTIMIZACIÓN CON PROGRAMACIÓN LINEAL
## Grupo 2: Dante Passone & Braian Tormey

---

## APERTURA (2 minutos)

**"Buenos días. Somos Dante Passone y Braian Tormey del Grupo 2, y hoy vamos a demostrar cómo la programación lineal puede transformar problemas empresariales complejos en soluciones óptimas mediante el uso de Python y PuLP."**

**"La programación lineal es una técnica matemática fundamental en investigación operativa que nos permite encontrar la mejor manera de asignar recursos limitados para maximizar o minimizar una función objetivo, siempre respetando un conjunto de restricciones lineales."**

**"En esta presentación, resolveremos dos problemas completamente diferentes: uno de logística educativa y otro de manufactura artesanal, demostrando la versatilidad y poder de esta metodología."**

---

## PROBLEMA 1: PAQUETES ESCOLARES (12 minutos)

### Enunciado (2 minutos)

**"Nuestro primer caso de estudio aborda un problema real de logística educativa. Unos almacenes quieren optimizar su oferta de material escolar para el inicio del curso académico."**

**"Disponen de un stock limitado: 600 cuadernos, 500 carpetas y 400 bolígrafos. El desafío es decidir cuántos paquetes de cada tipo fabricar para maximizar los ingresos, considerando que cada paquete tiene una composición específica y un precio de venta determinado."**

**"Este tipo de problema es típico en la gestión de inventarios y planificación de producción, donde debemos equilibrar la demanda del mercado con las limitaciones de recursos disponibles."**

### Modelo Matemático (3 minutos)

**"Para modelar este problema, definimos dos variables de decisión: x representa la cantidad de paquetes tipo 1, e y la cantidad de paquetes tipo 2. Estas son nuestras variables de control."**

**"La función objetivo que queremos maximizar es 6.5x + 7y, que representa el ingreso total. Cada coeficiente corresponde al precio de venta de cada tipo de paquete."**

**"Las restricciones surgen de las limitaciones físicas del stock. Para los cuadernos: 2x + 3y ≤ 600. Esta restricción asegura que no excedamos la disponibilidad de cuadernos, considerando que cada paquete tipo 1 usa 2 cuadernos y cada paquete tipo 2 usa 3."**

**"Similarmente, para las carpetas: x + y ≤ 500, ya que ambos tipos de paquetes usan exactamente una carpeta. Para los bolígrafos: 2x + y ≤ 400, donde el tipo 1 usa 2 bolígrafos y el tipo 2 usa solo 1."**

**"Finalmente, las restricciones de no negatividad x ≥ 0, y ≥ 0 son fundamentales porque no podemos fabricar cantidades negativas de paquetes."**

### Implementación en Python (4 minutos)

**"Ahora implementaremos este modelo usando Python y PuLP. PuLP es una biblioteca especializada en programación lineal que implementa algoritmos eficientes como el método simplex para encontrar soluciones óptimas."**

**"Primero, creamos un objeto LpProblem con el nombre 'Paquetes_Escolares' y especificamos que queremos maximizar la función objetivo. Esto inicializa el solver interno de PuLP."**

**"Definimos nuestras variables de decisión usando LpVariable. El parámetro lowBound=0 establece el límite inferior, cat='Integer' especifica que queremos soluciones enteras, lo cual es crucial en este contexto porque no podemos fabricar fracciones de paquetes."**

**"La función objetivo se define simplemente sumando los términos 6.5*x + 7*y. PuLP automáticamente reconoce esto como la función a maximizar."**

**"Las restricciones se agregan una por una usando el operador +=. Cada restricción tiene un nombre descriptivo que nos ayuda a identificar cuál es la limitación activa en la solución final."**

**"El método solve() ejecuta el algoritmo de optimización. PuLP internamente convierte nuestro problema a forma estándar y aplica el método simplex, que es matemáticamente garantizado para encontrar la solución óptima global si existe."**

### Resultados y Análisis (3 minutos)

**"La solución óptima encontrada es: 150 paquetes tipo 1 y 100 paquetes tipo 2, generando un ingreso total de 1.675 euros."**

**"Este resultado es matemáticamente óptimo, lo que significa que no existe ninguna otra combinación factible que genere mayor ingreso respetando todas las restricciones."**

**"El gráfico muestra la región factible como un polígono convexo. La solución óptima se encuentra en un vértice de este polígono, lo cual es una propiedad fundamental de la programación lineal: las soluciones óptimas siempre ocurren en los vértices de la región factible."**

**"Observamos que la restricción de bolígrafos es activa en la solución óptima, lo que significa que este recurso es el factor limitante. Las carpetas tienen un exceso significativo, indicando una oportunidad de optimización del inventario."**

---

## ANÁLISIS DE MEJORAS - PAQUETES ESCOLARES (3 minutos)

**"El análisis de sensibilidad nos permite evaluar el impacto de cambios en los parámetros del problema. Consideramos dos escenarios de mejora."**

**"En el primer escenario, aumentamos el stock de bolígrafos de 400 a 450 unidades. Este cambio permite fabricar más paquetes tipo 1, que son más rentables por unidad. El resultado muestra un incremento en la ganancia total."**

**"En el segundo escenario, reducimos el stock de carpetas de 500 a 250 unidades. Este análisis revela que las carpetas tienen un exceso significativo, por lo que esta reducción no afecta la ganancia pero sí reduce costos de almacenamiento y capital inmovilizado."**

**"Estos análisis demuestran el valor de la programación lineal no solo para encontrar soluciones óptimas, sino también para evaluar la robustez de estas soluciones ante cambios en las condiciones del problema."**

---

## PROBLEMA 2: JOYAS ARTESANALES (12 minutos)

### Enunciado (2 minutos)

**"Nuestro segundo caso de estudio aborda un problema de manufactura artesanal completamente diferente. Un orfebre debe optimizar la producción de joyas considerando limitaciones de metales preciosos."**

**"Este problema es representativo de industrias donde los recursos son costosos y escasos, y donde la optimización puede tener un impacto significativo en la rentabilidad del negocio."**

**"El orfebre dispone de 750 gramos de oro y 750 gramos de plata, y puede fabricar dos tipos de joyas con diferentes composiciones y precios de venta."**

### Modelo Matemático (3 minutos)

**"El modelo matemático para este problema es más simétrico que el anterior. Definimos x como la cantidad de joyas tipo A e y como la cantidad de joyas tipo B."**

**"La función objetivo 40x + 50y representa el beneficio total, donde cada coeficiente corresponde al precio de venta de cada tipo de joya."**

**"Las restricciones reflejan el consumo de metales preciosos. Para el oro: x + 1.5y ≤ 750, donde la joya tipo A consume 1 gramo y la tipo B consume 1.5 gramos."**

**"Para la plata: 1.5x + y ≤ 750, donde la joya tipo A consume 1.5 gramos y la tipo B consume 1 gramo. Esta simetría en las restricciones es matemáticamente interesante y nos llevará a una solución equilibrada."**

**"Las restricciones de no negatividad x ≥ 0, y ≥ 0 son igualmente importantes en este contexto."**

### Implementación en Python (4 minutos)

**"La implementación en Python sigue la misma metodología, pero ahora trabajamos con un problema donde ambas restricciones son igualmente importantes."**

**"Creamos un nuevo objeto LpProblem llamado 'Problema_Joyas' y definimos nuestras variables de decisión con las mismas especificaciones de enteros y no negatividad."**

**"La función objetivo 40*x + 50*y se define de manera similar. Las restricciones se implementan usando las ecuaciones matemáticas que derivamos del análisis del problema."**

**"El método solve() ejecuta el algoritmo de optimización. En este caso, el problema es más equilibrado, lo que se reflejará en la solución final."**

### Resultados y Análisis (3 minutos)

**"La solución óptima es: 300 joyas tipo A y 300 joyas tipo B, generando un beneficio total de 27.000 euros."**

**"Esta solución es matemáticamente elegante porque ambas restricciones son activas simultáneamente. Esto significa que tanto el oro como la plata se consumen completamente, sin excesos."**

**"El gráfico muestra que la solución óptima se encuentra en la intersección de las dos restricciones principales. Esta propiedad matemática es fundamental: cuando dos restricciones son activas, la solución se encuentra en su punto de intersección."**

**"La simetría de la solución (300 de cada tipo) refleja la simetría en las restricciones del problema. Este es un ejemplo clásico de cómo la estructura matemática del problema se refleja en la estructura de la solución."**

---

## ANÁLISIS DE MEJORAS - JOYAS (3 minutos)

**"El análisis de mejoras para este problema es diferente al anterior. Como no hay excesos de recursos, las mejoras deben venir de aumentar la disponibilidad de materiales."**

**"Consideramos el escenario de aumentar el stock a 900 gramos de oro y 900 gramos de plata. Este cambio permite fabricar 360 joyas de cada tipo, aumentando el beneficio total a 32.400 euros."**

**"Este análisis demuestra el concepto de rendimientos marginales decrecientes: el incremento en el beneficio no es proporcional al incremento en los recursos, debido a las restricciones lineales del problema."**

**"La visualización muestra cómo la región factible se expande, pero mantiene su forma geométrica fundamental, lo cual es una propiedad importante de la programación lineal."**

---

## CONCLUSIONES Y REFLEXIONES FINALES (3 minutos)

**"Hemos demostrado exitosamente cómo la programación lineal puede aplicarse a problemas empresariales muy diferentes, desde logística educativa hasta manufactura artesanal."**

**"Los dos problemas ilustran conceptos fundamentales: el primero muestra un problema con recursos desequilibrados donde una restricción es claramente limitante, mientras que el segundo muestra un problema equilibrado donde múltiples restricciones son activas simultáneamente."**

**"Python con PuLP demostraron ser herramientas excepcionalmente poderosas para implementar estos modelos. La combinación de simplicidad de uso y robustez matemática hace de esta tecnología una opción ideal para optimización empresarial."**

**"Los análisis de sensibilidad que realizamos son cruciales en la práctica empresarial, ya que permiten evaluar la robustez de las soluciones y identificar oportunidades de mejora."**

**"La programación lineal sigue siendo una de las herramientas más importantes en investigación operativa, con aplicaciones en logística, finanzas, manufactura, y muchos otros campos."**

---

## CIERRE (1 minuto)

**"En conclusión, hemos demostrado que la programación lineal, implementada con Python y PuLP, puede transformar problemas empresariales complejos en soluciones óptimas y cuantificables."**

**"La metodología que hemos presentado es aplicable a una amplia gama de problemas reales, y las herramientas que hemos utilizado están disponibles gratuitamente, democratizando el acceso a técnicas avanzadas de optimización."**

**"Gracias por su atención. ¿Hay alguna pregunta sobre nuestro trabajo o sobre las aplicaciones de la programación lineal en otros contextos?"**

---

## PUNTOS CLAVE PARA DESTACAR

1. **Dominio técnico:** Conocimiento profundo de algoritmos de optimización
2. **Análisis crítico:** Identificación de restricciones activas y oportunidades de mejora
3. **Aplicabilidad práctica:** Conexión clara entre teoría matemática y problemas reales
4. **Metodología sistemática:** Enfoque estructurado desde modelado hasta implementación
5. **Pensamiento analítico:** Capacidad de interpretar resultados y extraer insights
6. **Comunicación técnica:** Explicación clara de conceptos complejos

**¡PRESENTACIÓN COMPLETA Y PROFESIONAL! 🚀** 