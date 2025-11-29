## 1. Problema de Negocio

LendSmart se enfrenta actualmente a un desafío comercial crítico: una tasa de incumplimiento de préstamos del 28%, la cual la gerencia considera insosteniblemente alta. Esta alta tasa de incumplimiento resulta en pérdidas financieras directas y erosiona la rentabilidad.
Nuestro equipo fue contratado con el objetivo de analizar los datos históricos de riesgo crediticio de la compañía. La tarea consistió en construir y evaluar un modelo estadístico capaz de predecir la probabilidad de que un nuevo solicitante incumpla con su préstamo. El fin último es proporcionar a LendSmart una herramienta basada en datos para identificar a los solicitantes de alto riesgo antes de la aprobación del préstamo, reduciendo así las pérdidas por incumplimiento mientras se mantiene un nivel aceptable de aprobación de préstamos a clientes solventes.


## 2. Hallazgos Clave y Percepciones

Nuestro análisis de los datos históricos de los solicitantes reveló varios factores determinantes que influyen en el riesgo de incumplimiento.
El Puntaje de Crédito es el Factor Decisivo: Descubrimos que el puntaje de crédito (credit_score) de un solicitante es, con diferencia, el predictor individual más importante del riesgo. Un puntaje de crédito más bajo se correlaciona de manera abrumadora y directa con una mayor probabilidad de incumplimiento.
Otros Indicadores de Riesgo Significativos: Además del puntaje de crédito, otros dos factores destacaron:
Relación Deuda-Ingresos (debt_to_income_ratio): Los solicitantes con una proporción más alta de deuda existente en relación con sus ingresos anuales tienen más probabilidades de incumplir.
Valor de los Activos (assets_value): Un menor valor total de activos reportados también se asocia con un mayor riesgo.
En términos simples, el perfil de un solicitante de alto riesgo es típicamente alguien con un puntaje de crédito bajo, un alto nivel de deuda existente en comparación con sus ingresos y un bajo valor de activos.


## 3. Rendimiento y Selección del Modelo

Comparamos dos técnicas estadísticas principales para este problema: el Análisis Discriminante Lineal (LDA) y el Análisis Discriminante Cuadrático (QDA). Ambos modelos fueron entrenados y probados rigurosamente para determinar su efectividad en la separación de solicitantes "buenos" (pago) de "malos" (incumplimiento).
Aunque ambos modelos funcionaron excepcionalmente bien, seleccionamos el modelo de Análisis Discriminante Lineal (LDA) como nuestra recomendación final. El modelo LDA no solo logró un rendimiento casi perfecto, sino que también ofrece una mayor interpretabilidad y estabilidad, lo cual es crucial para la toma de decisiones de negocio.
El rendimiento del modelo LDA en nuestros datos de prueba fue sobresaliente y aborda directamente el problema principal de LendSmart:
Identificación de Incumplidores: El modelo identificó correctamente al 100% de los solicitantes que de hecho incumplirían (una Tasa de Falsos Negativos del 0%). Esto significa que el modelo es extremadamente eficaz en detectar el peor escenario posible: aprobar un préstamo "malo".
Protección de Clientes Solventes: El modelo también logró una Tasa de Falsos Positivos del 0%, lo que significa que no marcó incorrectamente a ningún solicitante "bueno" como de "alto riesgo".
En resumen, el modelo LDA demostró ser una herramienta increíblemente precisa para clasificar a los solicitantes, minimizando el riesgo financiero sin incurrir en costos de oportunidad al rechazar clientes solventes.


## 4. Recomendación Final

Recomendamos que LendSmart adopte e implemente el modelo LDA en su proceso de evaluación de solicitudes de préstamos para identificar a los solicitantes de alto riesgo.
El beneficio comercial principal de este modelo es la reducción drástica de las pérdidas por incumplimiento. Al identificar con éxito a todos los solicitantes de alto riesgo en nuestro conjunto de prueba, el modelo demuestra el potencial de reducir significativamente la tasa de incumplimiento del 28%.
El modelo logra el equilibrio comercial deseado: minimiza el peor escenario (aprobar un préstamo incobrable) a casi cero, sin sacrificar ingresos al rechazar erróneamente a solicitantes calificados.
Como siguiente paso inmediato, recomendamos implementar este modelo en un entorno de prueba o piloto. Esto permitirá a LendSmart monitorear su rendimiento con datos de aplicaciones en tiempo real y validar que su efectividad se mantiene antes de un despliegue completo en toda la organización.

Link video
https://youtu.be/wC3RTkFBZ1g


