# Proyecto de Predicción de Calidad del Sueño con Machine Learning

## Integrantes del Equipo

- **Yose Sotomayor** - A01750908
- **Carlos Zamudio** - A01799283
- **José Moreno** - A01747922
- **Daniel Bernal** - A01750047

## Descripción del Proyecto

Este proyecto implementa y compara **4 algoritmos de machine learning** para predecir la calidad del sueño basándose en características demográficas, hábitos de consumo de café, actividad física y salud de 10,000 personas. El dataset sintético incluye variables como edad, género, país, consumo de café, horas de sueño, BMI, frecuencia cardíaca, nivel de estrés, actividad física, problemas de salud, ocupación, tabaquismo y consumo de alcohol.

## Estructura del Proyecto

```
├── comparacion_modelos.ipynb             # Notebook principal con análisis completo
├── synthetic_coffee_health_10000.csv     # Dataset con 10,000 registros
└── requirements.txt                     # Dependencias del proyecto
```

## Características del Dataset

- **Tamaño**: 10,000 registros
- **Variables**: 15 características (demográficas, salud, hábitos)
- **Objetivo**: Predicción de calidad del sueño (4 clases: Excellent, Good, Fair, Poor)
- **Preprocesamiento**: Estandarización, codificación de variables categóricas, transformación 

## Técnicas de Machine Learning Utilizadas

- **Preprocesamiento**: StandardScaler, OneHotEncoder, PowerTransformer
- **Validación**: StratifiedKFold (5 folds)
- **Optimización**: GridSearchCV para hiperparámetros
- **Métricas**: Accuracy, F1-Score, Classification Report, Matrices de Confusión

## Conclusiones del Análisis de Modelos de Machine Learning

Se implementaron y compararon **4 algoritmos de machine learning** para predecir la calidad del sueño basándose en características demográficas, hábitos de consumo de café, actividad física y salud de 10,000 personas. Todos los modelos mostraron rendimientos muy buenos, superando el 98.8% de precisión.

### Resultados Principales

| Modelo | Accuracy | F1-Score | Tiempo Entrenamiento |
|--------|----------|----------|---------------------|
| **XGBoost** | **99.05%** | **99.05%** | 247.33s |
| **CatBoost** | 98.95% | 98.95% | 32.59s |
| **Random Forest** | 98.95% | 98.95% | 288.64s |
| **Neural Network** | 98.85% | 98.86% | 1.98s |

### Análisis y ventajas de cada modelo

#### **Mejor Modelo: XGBoost**
- **Precisión más alta**: 99.05% de accuracy y F1-score
- **Rendimiento**: Excelente clasificación en todas las categorías de calidad de sueño
- **Robustez**: Maneja bien las clases desbalanceadas (Good: 1162, Fair: 375, Excellent: 273, Poor: 190)

#### **Modelo Más Eficiente: Neural Network**
- **Velocidad superior**: Solo 1.98 segundos de entrenamiento
- **Rendimiento**: 98.85% de precisión

#### **Modelo Balanceado: CatBoost**
- **Rendimiento**: 98.95% de precisión en solo 32.59s
- **Manejo automático de variables categóricas**: Menos preprocesamiento requerido
- **Estabilidad**: Resultados consistentes y confiables

#### **Modelo Robusto: Random Forest**
- **Rendimiento**: 98.95% de accuracy
- **Interpretabilidad**: Fácil análisis de importancia de características
- **Resistencia al overfitting**: Múltiples árboles de decisión

### Limitaciones

- **Dataset sintético**: Los resultados pueden no reflejar completamente datos reales
- **Overfitting potencial**: Precisión muy alta puede indicar sobreajuste
- **Variables faltantes**: Algunas características importantes del sueño podrían no estar incluidas
