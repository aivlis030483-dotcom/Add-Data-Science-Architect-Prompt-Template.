# Add-Data-Science-Architect-Prompt-Template.
Plantilla de prompts optimizadas y estandarizadas bajo el modelo R-I-T-A para automatizar tareas críticas en pipelines de Ciencia de Datos y Análisis Exploratorio de Datos (EDA).
[ROL Y CONTEXTO]
Actúa como un Científico de Datos Senior y Arquitecto de Soluciones de Inteligencia Artificial. Tu objetivo es diseñar un pipeline automatizado de análisis exploratorio de datos (EDA) bajo estándares de código de producción, priorizando la robustez algorítmica, el aislamiento de errores y la reproducibilidad científica.

[INFORMACIÓN Y RESTRICCIONES]
- Formato de entrada: Un archivo de datos estructurado en formato {FORMATO_ENTRADA}.
- Stack tecnológico: Código puramente escrito en Python utilizando Pandas, NumPy y Scikit-learn para el procesamiento de datos, y Seaborn junto a Matplotlib para las salidas gráficas.
- Restricciones técnicas: El script debe seguir el paradigma funcional (modularizado en funciones con Type Hints explícitos), incluir bloques try-except para el manejo de excepciones de E/S o codificación, y procesar las columnas dinámicamente sin depender de nombres fijos o predefinidos.

[TAREA]
Genera un script de Python completo, limpio y documentado que divida el proceso en las siguientes fases secuenciales, verificando la consistencia e interpretando los hallazgos en cada etapa:
1. Control de Calidad de Datos (Data Quality Framework): Evalúa de forma exhaustiva la completitud del archivo. Diseña una estrategia paramétrica para el tratamiento de valores nulos (implementando alternativas como {ESTRATEGIA_NULOS}).
2. Tratamiento de Valores Atípicos (Outliers): Implementa una función técnica concreta para detectar y aislar valores atípicos utilizando el método del Rango Intercuartílico (IQR).
3. Estadística Descriptiva y Análisis de Patrones: Calcula las métricas estadísticas clave del dataset y genera hipótesis automáticas sobre tendencias o patrones correlativos ocultos entre las variables numéricas y categóricas.

[ADAPTABILIDAD]
Para asegurar que este prompt funcione como una plantilla reutilizable en entornos corporativos por otros profesionales, utiliza obligatoriamente las siguientes variables de configuración al inicio del código:
RUTA_ARCHIVO = "{RUTA_DEL_ARCHIVO}"
ESTRATEGIA_NULOS = "{ESTRATEGIA_NULOS}"  # Opciones admitidas: 'impute_mean', 'impute_median', 'drop'
UMBRAL_IQR = {UMBRAL_IQR}  # Parámetro por defecto: 1.5
