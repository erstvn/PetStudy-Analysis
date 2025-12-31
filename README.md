# Pet-Study-and-Analysis

This repository contains:

<ins>index.html</ins>: General analysis dashboard.  
<ins>training_model</ins>: Base code for running the training model to analyze the sample of 3000 entries from the PetFinder dataset.

### Key variables to analyze:
- Demographic: Species, breed, age, weight, sex
- Environmental: Type of housing, outdoor access, climate
- Care-related: Veterinary visit frequency, type of diet, physical activity
- Health: Chronic diseases, vaccination, sterilization

## Tentative analysis structure
### Phase 1: Descriptive Analysis
- Age distribution by species and breed
- Most common diseases by age group
- Geographic patterns in longevity

### Phase 2: Correlation Analysis
- Relationship between sterilization and life expectancy
- Impact of body weight on joint diseases
- Correlation between veterinary visits and early detection

### Phase 3: Predictive Modeling
```python
from pyspark.ml.regression import RandomForestRegressor
from pyspark.ml.feature import VectorAssembler

# Predict life expectancy based on key features
assembler = VectorAssembler(
    inputCols=['raza_encoded', 'peso', 'esterilizado', 'frecuencia_veterinario'],
    outputCol='features'
)
```

### Phase 4: Educational Visualization
- Interactive dashboard for pet owners
- Care guides by life stage
- Early alerts for common diseases

## References and initial datasets
- [PetFinder Dataset](https://www.kaggle.com/competitions/petfinder-adoption-prediction): Information on pets available for adoption (age, breed, medical history)
- Veterinary Medical Databases: Anonymous records of veterinary diagnoses
- Owner surveys: Data on feeding, exercise, and home environment
- Climate and geographic data: Influence of the environment on animal health
- Longitudinal studies on pet aging
