# 🎤 GUION COMPLETO - PRESENTACIÓN PAQUETES ESCOLARES

## **DIApositiva 1: APERTURA ÉPICA**
**Duración estimada: 45 segundos**

*"¡Bienvenidos al futuro de la optimización empresarial!*

*Hoy no solo les presentaremos un trabajo académico, sino que demostraremos cómo la tecnología moderna puede transformar datos simples en decisiones inteligentes que generan valor real.*

*Somos Dante Passone y Braian Tormey del Grupo 2, y estamos aquí para mostrarles el poder revolucionario de la programación lineal combinada con Python y PuLP.*

*Preparados para una demostración que cambiará su perspectiva sobre la toma de decisiones empresariales."*

---

## **DIApositiva 2: INTRODUCCIÓN**
**Duración estimada: 30 segundos**

*"Nuestro proyecto se centra en la 'Optimización de Paquetes Escolares usando Programación Lineal con Python'.*

*No es solo un ejercicio matemático, sino una simulación real de cómo las empresas toman decisiones estratégicas todos los días."*

---

## **DIApositiva 3: OBJETIVO DEL TRABAJO**
**Duración estimada: 45 segundos**

*"Nuestro trabajo tiene cinco objetivos ambiciosos:*

*• Primero, modelar un problema de optimización real que simula una situación empresarial auténtica*

*• Segundo, implementar la solución usando Python y la poderosa librería PuLP*

*• Tercero, visualizar la región factible y la solución óptima de manera intuitiva*

*• Cuarto, analizar mejoras y alternativas para optimizar aún más el negocio*

*• Y finalmente, demostrar el poder transformador de la programación lineal en la toma de decisiones"*

---

## **DIApositiva 4: ENUNCIADO DEL PROBLEMA**
**Duración estimada: 1 minuto**

*"El desafío que enfrentamos es fascinante:*

*Con el comienzo del curso escolar, unos almacenes quieren lanzar ofertas de material escolar. Disponen de recursos limitados: 600 cuadernos, 500 carpetas y 400 bolígrafos.*

*Pueden crear dos tipos de paquetes estratégicos:*

*• El paquete tipo 1 contiene 2 cuadernos, 1 carpeta y 2 bolígrafos, y se vende a 6,50 euros*

*• El paquete tipo 2 contiene 3 cuadernos, 1 carpeta y 1 bolígrafo, y se vende a 7,00 euros*

*La pregunta que resolveremos es crucial: ¿Cuántos paquetes de cada tipo deben fabricar para maximizar sus beneficios?*

*Este es exactamente el tipo de decisión que las empresas enfrentan diariamente."*

---

## **DIApositiva 5: DATOS IDENTIFICADOS**
**Duración estimada: 1 minuto**

*"Identificamos claramente los datos del problema:*

*• Stock disponible: 600 cuadernos, 500 carpetas y 400 bolígrafos - nuestros recursos limitados*

*• Dos tipos de paquetes con diferentes composiciones y precios - nuestras opciones estratégicas*

*• El objetivo es maximizar la ganancia respetando las limitaciones de stock - nuestro desafío*

*Estos datos nos permiten construir el modelo matemático que resolverá nuestro problema."*

---

## **DIApositiva 6: LÍMITES Y RESTRICCIONES**
**Duración estimada: 1 minuto 30 segundos**

*"Ahora definimos las restricciones matemáticas que gobiernan nuestro problema:*

*• Para cuadernos: 2x + 3y ≤ 600 - esto significa que la cantidad total de cuadernos usados no puede superar los 600*

*• Para carpetas: x + y ≤ 500 - no podemos usar más de 500 carpetas en total*

*• Para bolígrafos: 2x + y ≤ 400 - la suma de todos los bolígrafos no puede exceder 400*

*• Y las restricciones de no negatividad: x ≥ 0, y ≥ 0 - no se pueden fabricar cantidades negativas*

*Donde x representa los paquetes tipo 1 e y los paquetes tipo 2.*

*Estas restricciones definen nuestro espacio de posibilidades."*

---

## **DIApositiva 7: RESOLVIENDO CON PYTHON**
**Duración estimada: 45 segundos**

*"Para resolver este problema utilizamos Python junto con la librería PuLP, que es una herramienta especializada en programación lineal.*

*PuLP nos permite modelar y resolver problemas de optimización de forma eficiente, automatizando el proceso de búsqueda de la solución óptima.*

*Es como tener un supercomputador que analiza millones de combinaciones en segundos."*

---

## **DIApositiva 8: PREPARAR EL ENTORNO**
**Duración estimada: 30 segundos**

*"El primer paso es preparar nuestro entorno de trabajo:*

*• Instalamos PuLP usando pip - nuestra herramienta de optimización*

*• Importamos la librería para poder utilizarla*

*Esto nos da acceso a todas las herramientas necesarias para la optimización automática."*

---

## **DIApositiva 9: DEFINIR EL MODELO**
**Duración estimada: 1 minuto 30 segundos**

*"Ahora definimos nuestro modelo paso a paso:*

*• Paso 3: Creamos el problema de maximización con un nombre descriptivo*

*• Paso 4: Definimos las variables de decisión x e y como enteros no negativos*

*• Paso 5: Establecemos la función objetivo: 6.5x + 7y, que representa la ganancia total que queremos maximizar*

*Cada paso construye la base matemática de nuestro modelo de optimización."*

---

## **DIApositiva 10: RESTRICCIONES Y RESOLUCIÓN**
**Duración estimada: 1 minuto**

*"Continuamos con los pasos finales:*

*• Paso 6: Agregamos las tres restricciones que definimos anteriormente*

*• Paso 7: Ejecutamos el solver para encontrar la solución óptima*

*Con estos pasos, PuLP analiza todas las combinaciones posibles y encuentra la mejor solución en cuestión de milisegundos."*

---

## **DIApositiva 11: VER EL RESULTADO**
**Duración estimada: 45 segundos**

*"El paso 8 consiste en mostrar los resultados de forma clara:*

*• Verificamos que se encontró una solución óptima*

*• Mostramos cuántos paquetes de cada tipo fabricar*

*• Calculamos la ganancia total obtenida*

*Este código nos da la respuesta final a nuestro problema de optimización."*

---

## **DIApositiva 12: SOLUCIÓN ÓPTIMA**
**Duración estimada: 1 minuto**

*"¡Y aquí está nuestra solución óptima!*

*• Debemos fabricar 150 paquetes tipo 1*

*• Y 100 paquetes tipo 2*

*• Esto nos dará una ganancia total de 1.675 euros*

*Esta es la combinación que maximiza los beneficios respetando todas las restricciones de stock.*

*¡Hemos encontrado la estrategia ganadora!"*

---

## **DIApositiva 13: VISUALIZACIÓN GRÁFICA**
**Duración estimada: 1 minuto 30 segundos**

*"Para entender mejor la solución, creamos una visualización gráfica que muestra:*

*• Las líneas de restricción para cada recurso*

*• La región factible donde se cumplen todas las restricciones*

*• El punto óptimo donde se alcanza la ganancia máxima*

*• La línea de ganancia que pasa por la solución óptima*

*Este gráfico confirma visualmente que nuestra solución es correcta y nos ayuda a entender por qué es la mejor."*

---

## **DIApositiva 14: ANÁLISIS DE MEJORAS**
**Duración estimada: 45 segundos**

*"Pero no nos conformamos con la solución inicial. Como verdaderos analistas de optimización, analizamos dos escenarios de mejora:*

*• Aumentar el stock de bolígrafos en 50 unidades*

*• Reducir el stock de carpetas en 250 unidades*

*Esto nos permite optimizar aún más el negocio y demostrar el valor del análisis estratégico."*

---

## **DIApositiva 15: ESCENARIO 1 - MÁS BOLÍGRAFOS**
**Duración estimada: 1 minuto**

*"En el primer escenario, aumentamos los bolígrafos de 400 a 450 unidades.*

*Esto tiene sentido porque los bolígrafos son el recurso más limitante del problema.*

*Al tener más bolígrafos, podemos fabricar más paquetes tipo 1, que son los que generan mayor ganancia por unidad.*

*Es un ejemplo perfecto de cómo identificar y eliminar cuellos de botella."*

---

## **DIApositiva 16: GRÁFICO ACTUALIZADO - MÁS BOLÍGRAFOS**
**Duración estimada: 45 segundos**

*"Como pueden ver en este gráfico actualizado, la región factible se expande hacia la derecha, permitiendo fabricar más paquetes tipo 1.*

*La nueva solución óptima aprovecha mejor los recursos disponibles y demuestra el impacto de eliminar restricciones limitantes."*

---

## **DIApositiva 17: ESCENARIO 2 - MENOS CARPETAS**
**Duración estimada: 1 minuto**

*"En el segundo escenario, analizamos la posibilidad de reducir las carpetas de 500 a 250 unidades.*

*Esto se debe a que en la solución óptima original solo usamos 250 carpetas, dejando 250 sin utilizar.*

*Reducir el stock de carpetas no afectaría la ganancia, pero permitiría ahorrar costos de compra y almacenamiento.*

*Es un ejemplo de optimización de costos sin impacto en los beneficios."*

---

## **DIApositiva 18: GRÁFICO ACTUALIZADO - MENOS CARPETAS**
**Duración estimada: 45 segundos**

*"Este gráfico muestra que con menos carpetas, la región factible se mantiene igual en términos de ganancia, confirmando que podemos reducir costos sin afectar los beneficios.*

*Es una lección valiosa sobre la gestión eficiente de inventarios."*

---

## **DIApositiva 19: CONCLUSIONES Y APRENDIZAJES**
**Duración estimada: 2 minutos**

*"A través de este trabajo hemos llegado a varias conclusiones importantes:*

*• Primero, encontramos la solución óptima: 150 paquetes tipo 1 y 100 tipo 2, generando 1.675 euros de ganancia máxima*

*• Segundo, identificamos que los bolígrafos son el recurso más limitante del problema - el cuello de botella*

*• Tercero, descubrimos que se pueden optimizar costos reduciendo 250 carpetas sin afectar la ganancia*

*• Cuarto, demostramos que Python con PuLP resuelve en segundos lo que manualmente tomaría horas o incluso días*

*• Y finalmente, confirmamos que este tipo de optimización tiene aplicaciones reales en logística, producción, finanzas y muchos otros campos empresariales*

*Hemos transformado un problema complejo en una solución clara y accionable."*

---

## **DIApositiva 20: CIERRE ÉPICO**
**Duración estimada: 1 minuto**

*"¡Misión cumplida! Hemos logrado algo extraordinario:*

*• Encontramos la solución óptima que maximiza los beneficios*

*• Implementamos una solución tecnológica robusta y eficiente*

*• Realizamos un análisis completo que va más allá de la solución básica*

*• Demostramos el poder transformador de la programación lineal*

*Hemos transformado datos simples en decisiones inteligentes que generan valor real.*

*¿Hay alguna pregunta sobre nuestro trabajo revolucionario?"*

---

## **CONSEJOS PARA LA PRESENTACIÓN:**

### **🎯 ANTES DE PRESENTAR:**
- Practica el guión varias veces en voz alta con entusiasmo
- Cronometra cada sección para mantener el ritmo épico
- Prepara respuestas para posibles preguntas técnicas
- Verifica que todos los archivos funcionen correctamente
- Visualiza el éxito de la presentación

### **🎤 DURANTE LA PRESENTACIÓN:**
- Mantén contacto visual con la audiencia
- Usa un tono de voz claro, pausado y con entusiasmo
- Gesticula naturalmente para enfatizar puntos importantes
- Haz pausas dramáticas entre secciones clave
- Si te equivocas, continúa con naturalidad y confianza
- Transmite pasión por el tema

### **💡 TÉCNICAS DE PRESENTACIÓN ÉPICA:**
- Usa las transiciones de Reveal.js para crear impacto
- Apunta a elementos específicos en las diapositivas cuando los menciones
- En las diapositivas con código, explica brevemente qué hace cada línea
- En los gráficos, describe lo que ven antes de explicar las conclusiones
- Usa el tono épico especialmente en la apertura y cierre

### **⏱️ DISTRIBUCIÓN DEL TIEMPO:**
- **Total estimado:** 16-20 minutos
- **Apertura épica:** 1-2 minutos
- **Introducción:** 1-2 minutos
- **Desarrollo técnico:** 8-10 minutos  
- **Análisis de mejoras:** 3-4 minutos
- **Conclusiones:** 2-3 minutos
- **Cierre épico:** 1-2 minutos

### **🔧 PREPARACIÓN TÉCNICA:**
- Asegúrate de que el navegador funcione correctamente
- Ten un plan B por si falla la tecnología
- Prepara la presentación en modo pantalla completa
- Verifica que los gráficos se vean claramente
- Prueba las transiciones antes de la presentación

### **🌟 ELEMENTOS ÉPICOS A DESTACAR:**
- **Apertura:** "Futuro de la optimización empresarial"
- **Desarrollo:** "Poder revolucionario de la programación lineal"
- **Resultados:** "Solución óptima encontrada"
- **Cierre:** "Misión cumplida - Transformando datos en decisiones inteligentes"

**¡Estás listo para una presentación épica que dejará a todos impresionados! 🚀🏆** 