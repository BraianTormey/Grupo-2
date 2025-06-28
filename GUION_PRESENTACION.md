# 🎯 GUION PRESENTACIÓN - OPTIMIZACIÓN DE PAQUETES ESCOLARES Y JOYAS
## Grupo 2: Dante Passone & Braian Tormey

---

## 📋 **ESTRUCTURA DE LA PRESENTACIÓN**

### **DURACIÓN TOTAL:** 25-30 minutos
### **OBJETIVO:** Demostrar dominio de programación lineal con Python y PuLP en dos contextos diferentes

---

## 🚀 **SLIDE 1: APERTURA ÉPICA** (2 minutos)

### **Elementos que aparecen progresivamente:**
1. **Título principal:** "🚀 OPTIMIZACIÓN MÁXIMA"
2. **Subtítulo:** "El Poder de la Programación Lineal"
3. **Descripción:** "Transformando Datos en Decisiones Inteligentes"
4. **Tech Stack:** Python, PuLP, Optimización, Análisis
5. **Cierre:** "Preparados para revolucionar la toma de decisiones empresariales"

### **Guión:**
*"Buenos días, hoy vamos a demostrar cómo la programación lineal puede transformar datos en decisiones inteligentes. Utilizaremos Python y PuLP para resolver dos problemas reales de optimización empresarial."*

---

## 📦 **SLIDE 2: INTRODUCCIÓN** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "Optimización de Paquetes Escolares"
2. **Subtítulo:** "Programación Lineal con Python"
3. **Autores:** Dante Passone & Braian Tormey
4. **Grupo:** "Grupo 2 - Análisis de Optimización"

### **Guión:**
*"Somos Dante Passone y Braian Tormey del Grupo 2, y hoy resolveremos dos problemas de optimización: paquetes escolares y joyas artesanales, usando programación lineal con Python."*

---

## 🎯 **SLIDE 3: OBJETIVOS** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "Objetivo del Trabajo"
2. **Lista de objetivos** (aparecen uno por uno)

### **Guión:**
*"Nuestros objetivos son: modelar dos problemas reales, implementar las soluciones con Python y PuLP, visualizar las regiones factibles, analizar mejoras, y demostrar el poder de la programación lineal en diferentes contextos."*

---

## 📋 **SLIDE 4: ENUNCIADO PRIMER PROBLEMA** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Enunciado del Problema"
2. **Descripción del contexto**
3. **Paquete Tipo 1** (con precio)
4. **Paquete Tipo 2** (con precio)
5. **Pregunta clave**

### **Guión:**
*"El primer problema es el siguiente: Unos almacenes quieren ofrecer 600 cuadernos, 500 carpetas y 400 bolígrafos. Pueden crear dos tipos de paquetes: el Tipo 1 cuesta 6,50€ y contiene 2 cuadernos, 1 carpeta y 2 bolígrafos. El Tipo 2 cuesta 7,00€ y contiene 3 cuadernos, 1 carpeta y 1 bolígrafo. La pregunta es: ¿Cuántos paquetes de cada tipo deben hacer para maximizar los beneficios?"*

---

## 📊 **SLIDE 5: DATOS PRIMER PROBLEMA** (1.5 minutos)

### **Elementos progresivos:**
1. **Título:** "Datos Identificados"
2. **Subtítulo:** "Stock Disponible"
3. **Cuadernos:** 600
4. **Carpetas:** 500
5. **Bolígrafos:** 400
6. **Objetivo**

### **Guión:**
*"Identificamos los datos clave: tenemos 600 cuadernos, 500 carpetas y 400 bolígrafos disponibles. Nuestro objetivo es maximizar la ganancia respetando estas limitaciones de stock."*

---

## 🔒 **SLIDE 6: RESTRICCIONES PRIMER PROBLEMA** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Límites y Restricciones"
2. **Restricción de cuadernos:** 2x + 3y ≤ 600
3. **Restricción de carpetas:** x + y ≤ 500
4. **Restricción de bolígrafos:** 2x + y ≤ 400
5. **No negatividad:** x ≥ 0, y ≥ 0

### **Guión:**
*"Ahora formulamos las restricciones matemáticas. Para los cuadernos: 2x + 3y ≤ 600, donde x son paquetes tipo 1 e y son paquetes tipo 2. Para las carpetas: x + y ≤ 500. Para los bolígrafos: 2x + y ≤ 400. Y finalmente, x ≥ 0, y ≥ 0 porque no podemos fabricar cantidades negativas."*

---

## 🐍 **SLIDE 7-15: PYTHON PRIMER PROBLEMA** (8 minutos)

### **Guión detallado por sección:**

**SLIDE 7: Introducción Python**
*"Utilizaremos Python y la librería PuLP para resolver este problema. PuLP es una biblioteca especializada en programación lineal que nos permitirá modelar y resolver el problema de forma eficiente."*

**SLIDE 8: Preparar entorno**
*"Primero instalamos PuLP usando pip. Esta es la biblioteca que necesitamos para programación lineal. Luego importamos PuLP con el asterisco para tener acceso a todas sus funciones, y también matplotlib y numpy para visualización y cálculos."*

**SLIDE 9: Definir modelo**
*"Creamos un objeto LpProblem llamado 'Paquetes_Escolares'. LpMaximize indica que queremos maximizar la función objetivo. Definimos x como la cantidad de paquetes tipo 1, e y como la cantidad de paquetes tipo 2. El 0 indica el límite inferior, None significa sin límite superior, y LpInteger especifica que queremos números enteros. La función objetivo es 6.50x + 7.00y, que representa la ganancia total."*

**SLIDE 10: Restricciones**
*"Agregamos las restricciones una por una. La primera restringe el uso de cuadernos: 2x + 3y ≤ 600. La segunda restringe las carpetas: x + y ≤ 500. La tercera restringe los bolígrafos: 2x + y ≤ 400."*

**SLIDE 11: Resolver**
*"El método solve() ejecuta el algoritmo de programación lineal y encuentra la solución óptima."*

**SLIDE 12: Resultados**
*"Extraemos los valores de las variables óptimas. value(x) nos da la cantidad óptima de paquetes tipo 1, value(y) la cantidad de paquetes tipo 2, y value(prob.objective) la ganancia máxima."*

---

## 📊 **SLIDE 16-17: RESULTADOS PRIMER PROBLEMA** (2 minutos)

### **Guión:**
*"La solución óptima es: 150 paquetes tipo 1, 100 paquetes tipo 2, generando una ganancia total de 1.675 euros. Este gráfico muestra las restricciones como líneas, la región factible como área sombreada, y el punto óptimo donde se alcanza la ganancia máxima."*

---

## 🔍 **SLIDE 18-22: ANÁLISIS PRIMER PROBLEMA** (4 minutos)

### **Guión:**
*"Analizamos dos escenarios de mejora: aumentar el stock de bolígrafos en 50 unidades, y reducir el stock de carpetas en 250 unidades para ahorrar costos. En el primer escenario, aumentamos los bolígrafos de 400 a 450. Esto permite crear más paquetes tipo 1, que son más rentables. En el segundo escenario, reducimos las carpetas de 500 a 250. Observamos que hay un gran exceso de carpetas, por lo que esta reducción no afecta la ganancia pero sí reduce costos de almacenamiento."*

---

## 🎯 **SLIDE 23: CONCLUSIONES PRIMER PROBLEMA** (2 minutos)

### **Guión:**
*"Nuestras conclusiones del primer problema son: la solución óptima genera 1.675 euros, los bolígrafos son el recurso más limitante, las carpetas tienen exceso, y Python con PuLP demostraron ser herramientas poderosas para optimización."*

---

## 💎 **SLIDE 24: APERTURA SEGUNDO PROBLEMA** (1 minuto)

### **Guión:**
*"Ahora vamos a resolver un segundo problema completamente diferente: la optimización de joyas artesanales. Este problema nos mostrará cómo la programación lineal puede aplicarse en contextos muy distintos."*

---

## 💎 **SLIDE 25: ENUNCIADO SEGUNDO PROBLEMA** (2 minutos)

### **Guión:**
*"El segundo problema es el siguiente: Un orfebre fabrica dos tipos de joyas. Las del tipo A precisan 1 gr de oro y 1,5 gr de plata, vendiéndose a 40 euros cada una. Para la fabricación de las de tipo B emplea 1,5 gr de oro y 1 gr de plata, y las vende a 50 euros. El orfebre tiene solo en el taller 750 gr de cada uno de los metales. La pregunta es: ¿Cuántas joyas ha de fabricar de cada clase para obtener un beneficio máximo?"*

---

## 📊 **SLIDE 26-27: DATOS SEGUNDO PROBLEMA** (1.5 minutos)

### **Guión:**
*"Identificamos los datos clave: tenemos 750 gramos de oro y 750 gramos de plata disponibles. Nuestro objetivo es maximizar el beneficio respetando estas limitaciones de stock. Ahora formulamos las restricciones matemáticas. Para el oro: x + 1.5y ≤ 750, donde x son joyas tipo A e y son joyas tipo B. Para la plata: 1.5x + y ≤ 750. Y finalmente, x ≥ 0, y ≥ 0 porque no podemos fabricar cantidades negativas."*

---

## 🐍 **SLIDE 28-36: PYTHON SEGUNDO PROBLEMA** (8 minutos)

### **Guión detallado por sección:**

**SLIDE 28: Introducción Python**
*"Utilizaremos Python y la librería PuLP para modelar y resolver este problema de optimización de joyas mediante programación lineal."*

**SLIDE 29: Preparar entorno**
*"Primero instalamos PuLP usando pip. Luego importamos la librería PuLP para tener acceso a todas sus funciones."*

**SLIDE 30: Definir modelo**
*"Creamos un objeto LpProblem llamado 'Problema_Joyas'. LpMaximize indica que queremos maximizar la función objetivo. Definimos x como la cantidad de joyas tipo A, e y como la cantidad de joyas tipo B. El lowBound=0 indica el límite inferior, cat='Integer' especifica que queremos números enteros. La función objetivo es 40x + 50y, que representa el beneficio total."*

**SLIDE 31: Restricciones**
*"Agregamos las restricciones una por una. La primera restringe el uso de oro: x + 1.5y ≤ 750. La segunda restringe la plata: 1.5x + y ≤ 750."*

**SLIDE 32: Resolver**
*"El método solve() ejecuta el algoritmo de programación lineal y encuentra la solución óptima."*

**SLIDE 33: Resultados**
*"Verificamos si el problema se resolvió correctamente. 'Optimal' significa que se encontró la solución óptima. Extraemos los valores de las variables óptimas y mostramos los resultados."*

---

## 📊 **SLIDE 37-38: RESULTADOS SEGUNDO PROBLEMA** (2 minutos)

### **Guión:**
*"La solución óptima es: 300 joyas tipo A, 300 joyas tipo B, generando un beneficio total de 27.000 euros. Este gráfico muestra las restricciones de oro y plata, la región factible, la solución óptima y el punto donde se alcanza el beneficio máximo."*

---

## 🔍 **SLIDE 39-40: ANÁLISIS SEGUNDO PROBLEMA** (2 minutos)

### **Guión:**
*"En este caso, como no sobra material, es difícil pensar en mejoras directas. Las opciones serían aumentar el stock de oro y plata, o rediseñar las joyas para que usen menos recursos. El problema del orfebre es más equilibrado que el de paquetes escolares. Ambas restricciones (oro y plata) son limitantes, lo que hace que la solución óptima sea simétrica: 300 joyas de cada tipo. Esto demuestra que la programación lineal puede manejar diferentes tipos de problemas, desde desequilibrios de recursos hasta situaciones perfectamente balanceadas."*

---

## 🎯 **SLIDE 41: CONCLUSIONES FINALES** (2 minutos)

### **Guión:**
*"Nuestras conclusiones finales son: el primer problema generó 1.675 euros con bolígrafos como recurso limitante, el segundo problema generó 27.000 euros con oro y plata equilibrados. Esto nos muestra diferentes patrones: recursos limitantes versus recursos equilibrados. Python con PuLP demostraron ser herramientas poderosas para optimización en diferentes contextos. La programación lineal demostró ser una herramienta fundamental para la toma de decisiones empresariales en diferentes contextos."*

---

## 🏆 **SLIDE 42: CIERRE ÉPICO FINAL** (1 minuto)

### **Guión:**
*"Hemos completado exitosamente la optimización de dos problemas completamente diferentes, demostrando el poder de la programación lineal con Python. ¿Hay alguna pregunta sobre nuestro trabajo? Gracias por su atención."*

---

## 💡 **CONSEJOS PARA LA PRESENTACIÓN**

### **Antes de empezar:**
- ✅ Verificar que la presentación funcione correctamente
- ✅ Tener ambos códigos Python listos para ejecutar
- ✅ Preparar respuestas para preguntas técnicas

### **Durante la presentación:**
- ✅ Mantener contacto visual con la audiencia
- ✅ Usar las transiciones para enfatizar puntos clave
- ✅ Explicar el código línea por línea si el profesor lo solicita
- ✅ Demostrar confianza en el dominio del tema
- ✅ Destacar las diferencias entre ambos problemas

### **Posibles preguntas del profesor:**
1. **"¿Por qué usamos programación lineal?"** → Porque las restricciones y función objetivo son lineales
2. **"¿Qué diferencias hay entre ambos problemas?"** → Uno tiene recursos desequilibrados, otro equilibrados
3. **"¿Cómo verificamos que es la solución óptima?"** → PuLP usa algoritmos probados como el simplex
4. **"¿Qué otras aplicaciones tiene?"** → Logística, producción, finanzas, etc.
5. **"¿Por qué la solución del segundo problema es simétrica?"** → Porque ambas restricciones son igualmente limitantes

### **Tiempo estimado por sección:**
- Apertura: 2 min
- Introducción: 1 min
- Objetivos: 1 min
- Problema 1: 15 min
- Problema 2: 15 min
- Conclusiones: 2 min
- Cierre: 1 min

**TOTAL: 30 minutos**

---

## 🎯 **PUNTOS CLAVE A DESTACAR**

1. **Dominio técnico:** Conocimiento profundo de Python y PuLP
2. **Análisis crítico:** Identificación de mejoras y limitaciones en ambos problemas
3. **Visualización:** Comprensión gráfica de ambos problemas
4. **Aplicabilidad:** Relevancia en diferentes contextos empresariales
5. **Metodología:** Enfoque sistemático y profesional
6. **Comparación:** Análisis de diferencias entre problemas

**¡ÉXITO ASEGURADO! 🚀** 