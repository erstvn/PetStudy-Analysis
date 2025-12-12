
# Estudio-y-Analisis-de-Mascotas
Estudio de análisis sobre el impacto de medidas de prevencion y cuidado para lograr una mejor longevidad en mascotas.

El presente repositorio contiene:
- index.html: Dashboard de análisis general.
- analisis_detallado: Dashboard de análisis con métricas detalladas.
- modelo_entrenamiento: Código base de ejecución de modelo de entrenamiento para analizar la muestra de datos de 3000 ingresos provenientes del dataset PetFinder.

## METODOLOGÍAS USADAS

Fuentes de datos:
- Dataset PetFinder: Información de mascotas en adopción (edad, raza, historial médico)
- Veterinary Medical Databases: Registros anónimos de diagnósticos veterinarios
- Encuestas a dueños: Datos sobre alimentación, ejercicio, ambiente familiar
- Datos climáticos y geográficos: Influencia del entorno en la salud animal
- Estudios longitudinales sobre envejecimiento de mascotas

Variables clave a analizar:
- Demográficas: Especie, raza, edad, peso, sexo
- Ambientales: Tipo de vivienda, acceso al exterior, clima
- Cuidados: Frecuencia veterinaria, tipo de alimentación, actividad física
- Salud: Enfermedades crónicas, vacunación, esterilización

Estructura tentativa del análisis
Fase 1: Análisis Descriptivo
- Distribución de edades por especie y raza
- Enfermedades más comunes por grupo etario
- Patrones geográficos en la longevidad

Fase 2: Análisis de Correlación
- Relación entre esterilización y esperanza de vida
- Impacto del peso corporal en enfermedades articulares
- Correlación entre visitas veterinarias y detección temprana

Fase 3: Modelado Predictivo
```python
from pyspark.ml.regression import RandomForestRegressor
from pyspark.ml.feature import VectorAssembler

# Predecir esperanza de vida basado en características
assembler = VectorAssembler(
    inputCols=['raza_encoded', 'peso', 'esterilizado', 'frecuencia_veterinario'],
    outputCol='features'
)
```

Fase 4: Visualización Educativa
- Dashboard interactivo para dueños de mascotas
- Guías de cuidado por etapa de vida
- Alertas tempranas de enfermedades comunes


## Referencias y datasets iniciales
- PetFinder Dataset (Kaggle)
- Veterinary Medical Database (VMDB)
- Banfield Pet Hospital State of Pet Health
- AAHA Canine Life Stage Guidelines
- International Cat Care longevity studies
