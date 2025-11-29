# mi-portfolio-ma2003b
## Equipo no 7
Bertin Flores Silva A01660604 Ricardo Villarreal Bazán A01666859
En el presente portafolio se recompila las evidencias presentadas de tres diferentes casos de estudio. Los casos busca desarrollar habilidades de análisis, pensamiento critico, pensamiento lateral y creación de modelos. Cada caso esta orientado a una herramienta del análisis.

Abajo se presenta un desglose de los casos, los retos que los acompanan y las soluciones.

| Empresa / Caso |Problema de Negocio | Técnica Multivariada | Hallazgos y Resultados Clave|
| --- | --- | --- | --- |
| TechnoServe Solutions (Satisfacción del Cliente) | "Necesidad de entender qué impulsa la satisfacción y la renovación, dado que tenían 23 preguntas de encuesta y datos dispersos." | Análisis Factorial (Factor Analysis) | "Se redujeron 23 variables a 5 factores clave. Se descubrió que la ""Relación y Confianza"" (Factor 3) impacta más en el crecimiento de revenue que la calidad técnica." |
| MegaMart (Retail) | Falta de diferenciación de clientes; campañas masivas genéricas a pesar de tener datos de comportamiento. | Análisis de Conglomerados (Cluster Analysis / Segmentación) | "Se identificaron 5 segmentos distintos (ej. ""Leales de alto valor"" vs ""Exploradores nuevos""). Permite dejar el mensaje genérico y personalizar acciones de marketing."|
|LendSmart (Riesgo Crediticio) | Tasa de incumplimiento de préstamos insosteniblemente alta (28%) y necesidad de predecir fallos antes de aprobar. | Análisis Discriminante (LDA vs QDA) | "El Credit Score es el predictor más fuerte. El modelo LDA logró identificar al 100% de los incumplidores en la prueba (0% Falsos Negativos), recomendándose para implementación."|


|Característica | Análisis Factorial (Caso TechnoServe) | Análisis de Conglomerados / Cluster (Caso MegaMart) | Análisis Discriminante (Caso LendSmart) |
| --- | --- | --- | --- |
| Objetivo Principal | "Reducción de Dimensiones. Simplificar un gran número de variables en pocos ""conceptos"" o factores latentes." | Agrupación. Clasificar objetos (clientes) en grupos homogéneos entre sí y heterogéneos respecto a otros grupos. | Clasificación y Predicción. Predecir la pertenencia a un grupo predefinido (bueno/malo) basándose en variables predictoras. |
| Variable Dependiente |  No hay una variable dependiente explícita en la formación de factores; es una técnica de interdependencia. | "No hay variable dependiente (técnica no supervisada); los grupos se descubren, no se predefinen." | Sí existe (Categórica). Se conoce de antemano el grupo (ej. pagó vs. no pagó) y se busca la regla para clasificar. |
| ¿Cuándo es más efectiva? | Cuando tienes muchas variables correlacionadas (ej. encuestas largas) y necesitas encontrar temas subyacentes para simplificar el análisis. | "Cuando el mercado es heterogéneo y necesitas identificar perfiles naturales para estrategias diferenciadas (marketing, política)." | Cuando necesitas una regla de decisión clara para aprobar/rechazar o diagnosticar basándote en datos históricos etiquetados. |
| Resultado en el Caso | "Agrupó 23 preguntas en dimensiones como ""Calidad Técnica"" y ""Relación""." | "Segmentó 3,000 clientes en grupos como ""Leales"" o ""Buscadores de valor""." | Generó una función capaz de separar solicitantes solventes de los de alto riesgo con alta precisión. |


La Interpretabilidad sobre la ComplejidadEn el caso de LendSmart, se compararon modelos LDA y QDA. Aunque ambos funcionaron bien, se eligió LDA porque ofrece "mayor interpretabilidad y estabilidad", lo cual es crucial para explicar decisiones de negocio19.Lección: No siempre el modelo más complejo es el mejor. En negocios, poder explicar por qué se rechaza un crédito o se toma una decisión es tan valioso como la precisión matemática.

Los datos cuentan historias contraintuitivasEn el caso de TechnoServe, la intuición sugería que la "Calidad Técnica" (Factor 1) sería lo más importante para una empresa de soluciones. Sin embargo, el Análisis Factorial reveló que la "Relación y Confianza" (Factor 3) tenía una correlación más fuerte con el crecimiento de ingresos ($0.438$)20.Lección: El análisis multivariado sirve para romper sesgos internos. Sin el análisis factorial, la empresa habría seguido invirtiendo solo en capacitación técnica sin mejorar sus habilidades blandas21.

Del Análisis a la Acción (Operacionalización)El caso de MegaMart (Cluster) demuestra que encontrar los segmentos es solo la mitad del trabajo. El verdadero reto interpretativo es traducir "Grupo 1" en "Leales de Alto Valor" y asignarles una acción específica (Programa VIP)22222222.Lección: Un estudiante debe aprender que el "output" del software no es el resultado final. El resultado final es la etiqueta de negocio y la recomendación estratégica derivada de ese grupo estadístico23.

Validación y Métricas de ErrorEn LendSmart, el éxito no se midió solo por la exactitud general, sino por minimizar un tipo de error específico: los Falsos Negativos (aprobar un préstamo malo). El modelo logró 0% en esta métrica24.Lección: En clasificación (Discriminante), entender la matriz de confusión es vital. No todos los errores cuestan lo mismo; en banca, un falso negativo es mucho más costoso que un falso positivo.
