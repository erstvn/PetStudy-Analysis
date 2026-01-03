# Pet-Study-and-Analysis
![In Development](https://img.shields.io/badge/state-development-yellow) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

⚠️ **IMPORTANT: LICENSE UPDATE** ⚠️

**All versions of this project**, including commits and releases prior to this update, are now covered under the **Apache License 2.0**.

- ✅ Previous versions (v1.0, v0.5, etc.)
- ✅ All historical commits
- ✅ Past tags and releases
- ✅ Forks created before this date

**Effective Date**: [December 31, 2025]  
**Applicable License**: Apache License 2.0  
**Retroactive Coverage**: Yes

## This repository contains:

[index.html](index.html): General analysis dashboard.  

[training_model](training_model.py): Base code for running the training model to analyze the sample of 3000 entries from the PetFinder dataset.

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

## References and initial datasets
- [PetFinder Dataset](https://www.kaggle.com/competitions/petfinder-adoption-prediction): Information on pets available for adoption (age, breed, medical history)
- Veterinary Medical Databases: Anonymous records of veterinary diagnoses
- Owner surveys: Data on feeding, exercise, and home environment
- Climate and geographic data: Influence of the environment on animal health
- Longitudinal studies on pet aging
