# 🎯 GUION PRESENTACIÓN - OPTIMIZACIÓN DE PAQUETES ESCOLARES
## Grupo 2: Dante Passone & Braian Tormey

---

## 📋 **ESTRUCTURA DE LA PRESENTACIÓN**

### **DURACIÓN TOTAL:** 15-20 minutos
### **OBJETIVO:** Demostrar dominio de programación lineal con Python y PuLP

---

## 🚀 **SLIDE 1: APERTURA ÉPICA** (2 minutos)

### **Elementos que aparecen progresivamente:**
1. **Título principal:** "🚀 OPTIMIZACIÓN MÁXIMA"
2. **Subtítulo:** "El Poder de la Programación Lineal"
3. **Descripción:** "Transformando Datos en Decisiones Inteligentes"
4. **Tech Stack:** Python, PuLP, Optimización, Análisis
5. **Cierre:** "Preparados para revolucionar la toma de decisiones empresariales"

### **Guión:**
*"Buenos días, hoy vamos a demostrar cómo la programación lineal puede transformar datos en decisiones inteligentes. Utilizaremos Python y PuLP para resolver un problema real de optimización empresarial."*

---

## 📦 **SLIDE 2: INTRODUCCIÓN** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "Optimización de Paquetes Escolares"
2. **Subtítulo:** "Programación Lineal con Python"
3. **Autores:** Dante Passone & Braian Tormey
4. **Grupo:** "Grupo 2 - Análisis de Optimización"

### **Guión:**
*"Somos Dante Passone y Braian Tormey del Grupo 2, y hoy resolveremos un problema de optimización de paquetes escolares usando programación lineal con Python."*

---

## 🎯 **SLIDE 3: OBJETIVOS** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "Objetivo del Trabajo"
2. **Lista de objetivos** (aparecen uno por uno)

### **Guión:**
*"Nuestros objetivos son: modelar un problema real, implementar la solución con Python y PuLP, visualizar la región factible, analizar mejoras, y demostrar el poder de la programación lineal."*

---

## 📋 **SLIDE 4: ENUNCIADO** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Enunciado del Problema"
2. **Descripción del contexto**
3. **Paquete Tipo 1** (con precio)
4. **Paquete Tipo 2** (con precio)
5. **Pregunta clave**

### **Guión:**
*"El problema es el siguiente: Unos almacenes quieren ofrecer 600 cuadernos, 500 carpetas y 400 bolígrafos. Pueden crear dos tipos de paquetes: el Tipo 1 cuesta 6,50€ y contiene 2 cuadernos, 1 carpeta y 2 bolígrafos. El Tipo 2 cuesta 7,00€ y contiene 3 cuadernos, 1 carpeta y 1 bolígrafo. La pregunta es: ¿Cuántos paquetes de cada tipo deben hacer para maximizar los beneficios?"*

---

## 📊 **SLIDE 5: DATOS IDENTIFICADOS** (1.5 minutos)

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

## 🔒 **SLIDE 6: RESTRICCIONES** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Límites y Restricciones"
2. **Restricción de cuadernos:** 2x + 3y ≤ 600
3. **Restricción de carpetas:** x + y ≤ 500
4. **Restricción de bolígrafos:** 2x + y ≤ 400
5. **No negatividad:** x ≥ 0, y ≥ 0

### **Guión:**
*"Ahora formulamos las restricciones matemáticas. Para los cuadernos: 2x + 3y ≤ 600, donde x son paquetes tipo 1 e y son paquetes tipo 2. Para las carpetas: x + y ≤ 500. Para los bolígrafos: 2x + y ≤ 400. Y finalmente, x ≥ 0, y ≥ 0 porque no podemos fabricar cantidades negativas."*

---

## 🐍 **SLIDE 7: PYTHON** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "Resolviendo con Python"
2. **Descripción de herramientas**
3. **Logo de Python**
4. **Explicación de PuLP**

### **Guión:**
*"Utilizaremos Python y la librería PuLP para resolver este problema. PuLP es una biblioteca especializada en programación lineal que nos permitirá modelar y resolver el problema de forma eficiente."*

---

## 🔧 **SLIDE 8: PREPARACIÓN DEL ENTORNO** (2 minutos)

### **Código detallado línea por línea:**

```python
# Paso 1: Instalar PuLP
pip install pulp
```

**Explicación:** *"Primero instalamos PuLP usando pip. Esta es la biblioteca que necesitamos para programación lineal."*

```python
# Paso 2: Importar las librerías necesarias
from pulp import *
import matplotlib.pyplot as plt
import numpy as np
```

**Explicación:** *"Importamos PuLP con el asterisco para tener acceso a todas sus funciones. También importamos matplotlib para visualización y numpy para cálculos numéricos."*

---

## 📝 **SLIDE 9: DEFINICIÓN DEL MODELO** (3 minutos)

### **Código detallado línea por línea:**

```python
# Paso 3: Crear el problema de maximización
prob = LpProblem("Paquetes_Escolares", LpMaximize)
```

**Explicación:** *"Creamos un objeto LpProblem llamado 'Paquetes_Escolares'. LpMaximize indica que queremos maximizar la función objetivo."*

```python
# Paso 4: Definir las variables de decisión
x = LpVariable("Paquetes_Tipo_1", 0, None, LpInteger)
y = LpVariable("Paquetes_Tipo_2", 0, None, LpInteger)
```

**Explicación:** *"Definimos x como la cantidad de paquetes tipo 1, e y como la cantidad de paquetes tipo 2. El 0 indica el límite inferior, None significa sin límite superior, y LpInteger especifica que queremos números enteros."*

```python
# Paso 5: Definir la función objetivo
prob += 6.50*x + 7.00*y, "Ganancia_Total"
```

**Explicación:** *"La función objetivo es 6.50x + 7.00y, que representa la ganancia total. Cada paquete tipo 1 genera 6,50€ y cada paquete tipo 2 genera 7,00€."*

---

## 🔒 **SLIDE 10: RESTRICCIONES** (2 minutos)

### **Código detallado línea por línea:**

```python
# Paso 6: Agregar las restricciones
# Restricción de cuadernos
prob += 2*x + 3*y <= 600, "Cuadernos"

# Restricción de carpetas  
prob += x + y <= 500, "Carpetas"

# Restricción de bolígrafos
prob += 2*x + y <= 400, "Boligrafos"
```

**Explicación:** *"Agregamos las restricciones una por una. La primera restringe el uso de cuadernos: 2x + 3y ≤ 600. La segunda restringe las carpetas: x + y ≤ 500. La tercera restringe los bolígrafos: 2x + y ≤ 400."*

---

## ⚡ **SLIDE 11: RESOLUCIÓN** (1 minuto)

### **Código detallado línea por línea:**

```python
# Paso 7: Resolver el problema
prob.solve()
```

**Explicación:** *"El método solve() ejecuta el algoritmo de programación lineal y encuentra la solución óptima."*

```python
# Paso 8: Verificar el estado de la solución
print("Estado:", LpStatus[prob.status])
```

**Explicación:** *"Verificamos si el problema se resolvió correctamente. 'Optimal' significa que se encontró la solución óptima."*

---

## 📊 **SLIDE 12: RESULTADOS** (2 minutos)

### **Código detallado línea por línea:**

```python
# Paso 9: Mostrar los resultados
print("Paquetes Tipo 1:", value(x))
print("Paquetes Tipo 2:", value(y))
print("Ganancia Total: €", value(prob.objective))
```

**Explicación:** *"Extraemos los valores de las variables óptimas. value(x) nos da la cantidad óptima de paquetes tipo 1, value(y) la cantidad de paquetes tipo 2, y value(prob.objective) la ganancia máxima."*

### **Resultados esperados:**
- **Paquetes Tipo 1:** 150
- **Paquetes Tipo 2:** 100  
- **Ganancia Total:** €1.675

### **Guión:**
*"La solución óptima es: 150 paquetes tipo 1, 100 paquetes tipo 2, generando una ganancia total de 1.675 euros."*

---

## 📈 **SLIDE 13: VISUALIZACIÓN** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Visualización Gráfica"
2. **Descripción del gráfico**
3. **Leyenda:** Cuadernos, Carpetas, Bolígrafos
4. **Gráfico mostrado**

### **Guión:**
*"Este gráfico muestra las restricciones como líneas, la región factible como área sombreada, y el punto óptimo donde se alcanza la ganancia máxima. La región factible es el área donde se cumplen todas las restricciones."*

---

## 🔍 **SLIDE 14: ANÁLISIS DE MEJORAS** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Análisis de Mejoras"
2. **Descripción de escenarios**
3. **Aumentar Stock** (+50 bolígrafos)
4. **Reducir Costos** (-250 carpetas)

### **Guión:**
*"Analizamos dos escenarios de mejora: aumentar el stock de bolígrafos en 50 unidades, y reducir el stock de carpetas en 250 unidades para ahorrar costos."*

---

## 📈 **SLIDE 15: ESCENARIO 1** (1.5 minutos)

### **Guión:**
*"En el primer escenario, aumentamos los bolígrafos de 400 a 450. Esto permite crear más paquetes tipo 1, que son más rentables. El resultado muestra que la ganancia aumenta significativamente."*

---

## 📊 **SLIDE 16: GRÁFICO ESCENARIO 1** (1 minuto)

### **Guión:**
*"El gráfico actualizado muestra cómo la restricción de bolígrafos se desplaza, expandiendo la región factible y permitiendo una solución óptima con mayor ganancia."*

---

## 💰 **SLIDE 17: ESCENARIO 2** (1.5 minutos)

### **Guión:**
*"En el segundo escenario, reducimos las carpetas de 500 a 250. Observamos que hay un gran exceso de carpetas, por lo que esta reducción no afecta la ganancia pero sí reduce costos de almacenamiento."*

---

## 📊 **SLIDE 18: GRÁFICO ESCENARIO 2** (1 minuto)

### **Guión:**
*"Este gráfico muestra que la restricción de carpetas no es limitante, confirmando que podemos reducir el stock sin afectar la ganancia."*

---

## 🎯 **SLIDE 19: CONCLUSIONES** (2 minutos)

### **Elementos progresivos:**
1. **Título:** "Conclusiones y Aprendizajes"
2. **Solución Óptima:** 150 + 100 = €1.675
3. **Análisis de Recursos:** Bolígrafos limitantes
4. **Mejoras Identificadas:** +50 bolígrafos o -250 carpetas
5. **Herramientas Utilizadas:** Python + PuLP

### **Guión:**
*"Nuestras conclusiones son: la solución óptima genera 1.675 euros, los bolígrafos son el recurso más limitante, las carpetas tienen exceso, y Python con PuLP demostraron ser herramientas poderosas para optimización."*

---

## 🏆 **SLIDE 20: CIERRE ÉPICO** (1 minuto)

### **Elementos progresivos:**
1. **Título:** "MISIÓN CUMPLIDA"
2. **Subtítulo:** "Optimización Exitosamente Lograda"
3. **Badges de logros**
4. **Información de contacto**
5. **Mensaje final**

### **Guión:**
*"Hemos completado exitosamente la optimización, demostrando el poder de la programación lineal con Python. ¿Hay alguna pregunta sobre nuestro trabajo? Gracias por su atención."*

---

## 💡 **CONSEJOS PARA LA PRESENTACIÓN**

### **Antes de empezar:**
- ✅ Verificar que la presentación funcione correctamente
- ✅ Tener el código Python listo para ejecutar
- ✅ Preparar respuestas para preguntas técnicas

### **Durante la presentación:**
- ✅ Mantener contacto visual con la audiencia
- ✅ Usar las transiciones para enfatizar puntos clave
- ✅ Explicar el código línea por línea si el profesor lo solicita
- ✅ Demostrar confianza en el dominio del tema

### **Posibles preguntas del profesor:**
1. **"¿Por qué usamos programación lineal?"** → Porque las restricciones y función objetivo son lineales
2. **"¿Qué pasaría si cambiamos los precios?"** → Se modificaría la pendiente de la función objetivo
3. **"¿Cómo verificamos que es la solución óptima?"** → PuLP usa algoritmos probados como el simplex
4. **"¿Qué otras aplicaciones tiene?"** → Logística, producción, finanzas, etc.

### **Tiempo estimado por sección:**
- Apertura: 2 min
- Introducción: 1 min
- Objetivos: 1 min
- Enunciado: 2 min
- Datos: 1.5 min
- Restricciones: 2 min
- Python: 1 min
- Código: 8 min
- Resultados: 2 min
- Visualización: 2 min
- Análisis: 4 min
- Conclusiones: 2 min
- Cierre: 1 min

**TOTAL: 20 minutos**

---

## 🎯 **PUNTOS CLAVE A DESTACAR**

1. **Dominio técnico:** Conocimiento profundo de Python y PuLP
2. **Análisis crítico:** Identificación de mejoras y limitaciones
3. **Visualización:** Comprensión gráfica del problema
4. **Aplicabilidad:** Relevancia en el mundo real
5. **Metodología:** Enfoque sistemático y profesional

**¡ÉXITO ASEGURADO! 🚀** 