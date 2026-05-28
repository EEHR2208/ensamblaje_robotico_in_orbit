## FASE 1: Mapeo de Entidades (Análisis)

Al analizar el contexto de LaTeX de la sección de "Implementación y Simulación", se identifican las siguientes variables, relaciones y el nivel de abstracción del gráfico solicitado (`fig4.png`):

* **Entidades de Datos (Variables Dependientes):** Tiempo acumulado (segundos) y Consumo energético acumulado (kJ).
* **Factores de Comparación (Variables Independientes):** Configuración Mono-brazo (1 brazo) frente a Configuración Dual-brazo (2 brazos cooperativos).
* **Comportamiento Dinámico Esperado (Sección 4.2 y 4.3):** * **Tiempo:** La configuración dual-brazo completa las tareas sustancialmente más rápido (un 50% de reducción de tiempo promedio según la Tabla 2 para el Panel Solar: $1840\text{ s} \to 920\text{ s}$). Por tanto, la curva de tiempo dual-brazo debe ser notablemente más corta y con mayor pendiente inicial.
* **Energía:** El enfoque dual-brazo consume menos energía global gracias al uso de trayectorias híbridas más suaves y menor corrección reactiva ($215\text{ kJ} \to 187\text{ kJ}$, reducción del 22% reportada en el texto).


* **Nivel de Abstracción:** Gráfico cuantitativo de resultados/métricas de rendimiento mecánico-eléctrico orientado a publicaciones indexadas.

---

## FASE 2: Auditoría y Reporte de Hallazgos Críticos

### 1. Contraste de Coherencia

El prompt base acierta en la estética limpia, minimalista y bicolor. Sin embargo, comete errores de conceptualización gráfica que degradan la precisión científica requerida en entornos académicos y confunde el formato estándar de presentación de datos multivariable.

### 2. LISTA DE DISCREPANCIAS (Explícita)

* **Texto Incrustado (Conflicto Crítico):** El prompt base solicita *"sin texto incrustado"*. Un gráfico técnico IEEE **requiere obligatoriamente** etiquetas de texto para la nomenclatura de los ejes ($X$, $Y$), unidades físicas explícitas (s, kJ) y leyendas claras. Un gráfico de líneas sin texto carece de valor científico.
* **Ambigüedad en la Disposición de Ejes:** El prompt pide "dos curvas superiores y dos curvas inferiores" en un esquema plano de líneas múltiples. Graficar tiempo y energía (unidades diferentes: segundos vs. kiloJoules) en un único eje de ordenadas ($Y$) sin una separación clara o un eje $Y$ secundario es un error metodológico.
* **Falta de Representación de Compromisos (Sección 4.3):** El texto menciona que ante "perturbaciones fuertes" el sistema prioriza seguridad introduciendo pequeñas desviaciones o mesetas en la suavidad de la curva. El prompt base asume curvas perfectas e ideales, omitiendo el comportamiento real del framework bajo perturbaciones simuladas en Gazebo.

### 3. Control de Estilo

Se aplicará el formato riguroso de gráficos de la sociedad IEEE Robotics and Automation:

* Tipografía limpia Sans-Serif (`Helvetica` o `Arial`).
* **Azul Cobalto (`#0047AB`)** asignado exclusivamente a la propuesta principal del artículo: **Configuración Dual-brazo Cooperativo**.
* **Gris Técnico (`#4A4A4A`)** asignado a la línea base de control: **Configuración Mono-brazo**.
* Inclusión obligatoria de rejilla tenue (grid) y marcas de graduación.

---

## FASE 3: Explicación y Justificación de Pre-ejecución

### 1. Disposición Espacial y Elementos Gráficos

Para evitar la confusión de unidades, la figura se estructurará como un panel compuesto de dos sub-gráficos alineados verticalmente (Sub-gráfico A superior y Sub-gráfico B inferior) compartiendo el mismo eje de abscisas ($X$):

* **Eje X Común (Inferior):** Progreso del Ensamblaje estructural (%), mapeado desde el inicio (0%) hasta la completación (100%).
* **Gráfico Superior - Tiempo Acumulado (s):**
* *Línea Gris (#4A4A4A):* Mono-brazo. Trayectoria lineal-ascendente prolongada que finaliza en un valor alto de tiempo.
* *Línea Azul (#0047AB):* Dual-brazo. Curva optimizada que alcanza el 100% del ensamblaje en prácticamente la mitad del tiempo respecto a la gris.


* **Gráfico Inferior - Consumo Energético Acumulado (kJ):**
* *Línea Gris (#4A4A4A):* Curva escalonada con picos abruptos que evidencian las "correcciones reactivas" ante perturbaciones.
* *Línea Azul (#0047AB):* Curva continua y suavizada que representa la optimización del algoritmo híbrido y las trayectorias fluidas, finalizando un 22% por debajo de la línea gris.


* **Leyenda Única:** Cuadro técnico en la esquina superior derecha indicando la correspondencia de colores.

### 2. Justificación Técnica

Esta composición bicapa es la única alternativa válida que respeta la coherencia matemática y dimensional de las variables (tiempo y energía). Visualizar la reducción de pendiente y la finalización temprana de la línea azul cobalto valida inmediatamente ante el lector la eficiencia del framework híbrido propuesto sin necesidad de recurrir al texto de la sección 4.3.

### 3. ADVERTENCIAS PARA EL USUARIO (Validación)

Por favor, confirma las siguientes decisiones de diseño antes de generar el prompt final:

1. **Idioma de los Rótulos:** Al igual que en las fases de arquitectura, los ejes de las figuras científicas suelen requerirse en inglés. ¿Rotulamos los ejes como *"Accumulated Time (s)"* / *"Energy Consumption (kJ)"* o prefieres mantenerlos fiel al texto en español (*"Tiempo Acumulado (s)"* / *"Consumo Energético (kJ)"*)?
2. **Formato de Panel Integrado vs. Eje Y Doble:** He propuesto dividir la figura en dos sub-gráficos apilados verticalmente (estilo panel) porque es visualmente más limpio para vectores 2D planos. La otra opción es un único gráfico con un eje $Y$ a la izquierda (Tiempo) y un eje $Y$ a la derecha (Energía). ¿Confirmas el formato de panel apilado verticalmente?

---

**Una vez me des tus indicaciones sobre el idioma y la estructura del gráfico, procederé de inmediato con la Fase 4 para entregarte los prompts optimizados.**