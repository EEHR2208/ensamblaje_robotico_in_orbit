## FASE 1: Mapeo de Entidades (Análisis)

Al analizar el fragmento de LaTeX proporcionado para la sección "Resultados y Análisis", se identifican las siguientes variables cinemáticas, de control y de seguridad a un nivel de abstracción cuantitativo y comparativo (`fig5.png`):

* **Entidades de Rendimiento (Métricas Activas):** * *Reducción de Tiempo de Ensamblaje (% o segundos):* Evidencia una caída del 50% en el caso base ($1840\text{ s} \to 920\text{ s}$) y supera la planificación genética tradicional ($2150\text{ s}$).
* *Índice de Riesgo Compuesto / Probabilidad de Riesgo:* Integra probabilidad de colisión, pérdida de estabilidad e inercia y consumo excesivo. Reporta una reducción media del 47% al activar la configuración propuesta.


* **Factores de Estratificación (Variables Independientes):**
* *Configuraciones:* Mono-brazo tradicional frente a Framework Propuesto (Dual-brazo + Gemelo Digital).
* *Niveles de Perturbación:* Simulación Monte Carlo (Nominal, Perturbación Moderada, Perturbación Elevada/Extrema).


* **Comportamiento Crítico Degradado (Sección 5.2):** Robustez superior a perturbaciones elevadas (tasa de éxito $>85\%$), pero con una degradación más rápida (pendiente negativa pronunciada) al cruzar el umbral crítico del 12% de ruido en sensores LIDAR.

---

## FASE 2: Auditoría y Reporte de Hallazgos Críticos

### 1. Contraste de Coherencia

El prompt base propone mezclar en un formato ambiguo barras agrupadas a la izquierda y curvas de riesgo a la derecha. En una figura indexada IEEE monocromática o de paleta muy limitada, esta disposición en un solo lienzo sin estructuración formal satura los ejes y rompe el principio de legibilidad a un vistazo.

### 2. LISTA DE DISCREPANCIAS (Explícita)

* **Texto Omitido (Conflicto Crítico de Validación):** El prompt base exige *"sin texto incrustado"*. Para la figura `fig5.png`, es mecánicamente imposible mapear la reducción de riesgo del 47%, los niveles de perturbación de las simulaciones Monte Carlo o el umbral del 12% de ruido sin texto explícito en etiquetas, leyendas y nombres de ejes.
* **Invisibilidad del Punto de Quiebre Técnico (LIDAR 12%):** El análisis de robustez de la sección 5.2 describe un hallazgo crítico: la degradación acelerada del sistema a partir de un ruido superior al 12%. El prompt base ignora por completo esta frontera del análisis de sensibilidad, privando al gráfico de su utilidad interpretativa principal.
* **Indisponibilidad de Referencia de la Literatura:** La Tabla 3 incluye un contraste directo con la literatura activa (Timmermann 2024). El prompt de imagen solo contempla el contraste interno mono-brazo vs. dual-brazo, omitiendo la validación externa del framework contra el estado del arte.

### 3. Control de Estilo

Se fuerza la estructura estricta de diagramas estadísticos IEEE:

* Tipografía limpia, uniforme y vectorizada Sans-Serif.
* Uso de **Azul Cobalto (`#0047AB`)** para denotar el rendimiento superior del *Framework Propuesto (Dual-brazo)*.
* Uso de **Gris Técnico (`#4A4A4A`)** para trazar el comportamiento de la *Planificación Tradicional / Mono-brazo*.
* Eliminación total de efectos estéticos tridimensionales, sombras o degradados comerciales.

---

## FASE 3: Explicación y Justificación de Pre-ejecución

### 1. Disposición Espacial y Direccionalidad

La figura se organizará como un panel yuxtapuesto simétrico de dos gráficos independientes (Estructura de Panel Lado a Lado: Fig. 5a y Fig. 5b) para mantener la limpieza formal:

* **Gráfico Izquierdo (5a) - Eficiencia Temporal (Diagrama de Barras Agrupadas):**
* *Eje X:* Tres escenarios de carga de trabajo: "Panel Solar", "Truss Telescopio" y "Estación de Servicio".
* *Eje Y:* Tiempo total de operación (segundos).
* *Visualización:* Dos barras adyacentes por escenario. La barra gris (`#4A4A4A`, Configuración Mono-brazo) será el doble de alta que la barra azul (`#0047AB`, Framework Propuesto Dual), evidenciando la reducción de tiempo en órbita.


* **Gráfico Derecho (5b) - Análisis de Sensibilidad y Riesgo (Gráfico de Líneas de Tendencia):**
* *Eje X:* Intensidad de perturbaciones / Ruido del Sensor (%). Se marca explícitamente el límite del **12%**.
* *Eje Y:* Índice de Riesgo Compuesto (%).
* *Visualización:* La curva gris (Mono-brazo) inicia alta y sube exponencialmente hacia zonas de peligro. La curva azul (Framework Propuesto) inicia un 47% más abajo y mantiene una trayectoria sub-horizontal estable hasta el umbral del 12%, donde se muestra de forma explícita el cambio de pendiente (degradación controlada).



### 2. Justificación Técnica

La segmentación en un panel binario (Eficiencia vs. Robustez) permite al lector correlacionar los dos hallazgos principales del paper de forma inmediata: primero, que el sistema duplica la velocidad (5a), y segundo, que el gemelo digital en conjunción con el control híbrido amortigua el riesgo incluso cuando el entorno orbital se vuelve hostil (5b), registrando con rigor el comportamiento real de las simulaciones de Monte Carlo.

### 3. ADVERTENCIAS PARA EL USUARIO (Validación)

Antes de redactar la estructura final del prompt optimizado, requiero tu confirmación en los siguientes puntos de fricción:

1. **Idioma Técnico de Rótulos:** Para mantener homogeneidad profesional, ¿los sub-gráficos se etiquetarán en inglés (*"Assembly Configuration Efficiency"* / *"Risk & Robustness Analysis"*) o prefieres que los ejes utilicen español nativo acorde al texto?
2. **Inclusión de la Referencia Externa:** ¿Deseas agregar una tercera línea o barra testigo que represente los datos de la "Planificación Genética Estándar (Timmermann 2024)" para demostrar gráficamente que supera a la literatura, o limitamos el gráfico estrictamente al caso Mono-brazo vs. Dual-brazo?

---

**Por favor, confírmame tus preferencias de idioma y volumen de datos para proceder a la Fase 4 y entregarte los bloques de código con los prompts de ingeniería optimizados.**