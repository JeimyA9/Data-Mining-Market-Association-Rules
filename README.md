# Real Market Data con Reglas de asociación y detección de anomalias Data Mining

El dataset escogido se llama “Real Market Data for Association Rules” 
Link: https://www.kaggle.com/datasets/rukenmissonnier/real-market-data 

## Objetivo

El objetivo de este análisis es implementar el algoritmo Apriori para descubrir qué artículos tienden a comprarse juntos, evaluando su calidad mediante métricas de Soporte, Confianza y Sustento (Lift). Se aplicó modelo no supervisado Isolation Forest para aislar transacciones 
que se desvían del comportamiento promedio del consumidor.

## Enfoque Técnico

- **Limpieza de datos:** verificación de nulos, datos faltantes o duplicados
- **Minería de reglas de asociación:** exploración por niveles que identifica primero los ítems individuales más frecuentes y los combina progresivamente para encontrar patrones de coocurrencia 
- **Detección de anomalías:** Isolation Forest para identificar patrones extremos frente a patrones más sutiles.
- **Visualización:** Se utilizó PCA para la visualización dado que cada producto en la matriz binarizada representa una dimensión distinta

## Tecnologías

- Python
- scikit-learn (Isolation Forest)
- pandas / numpy
- matplotlib (visualización de EDA)
- mlxtend.frequent_patterns

## Resultados

-  La presencia de reglas con un Lift > 7.0 y niveles de Confianza > 80% confirma que existen relaciones de dependencia genuinas entre los productos analizados y no coincidencias estocásticas
- Isolation Forest logró separar con claridad las transacciones extremas del comportamiento modal del mercado
- Visualización mediante PCA:
- ![alt text](image.png)

## Estructura del Repositorio

```
├── data/                  # Dataset 
├── notebooks/             # Análisis exploratorio y modelado
├── src/                   # Scripts de preprocesamiento y modelos
└── README.md
```

## Cómo ejecutar

```bash
pip install -r requirements.txt
jupyter notebook notebooks/analisis.ipynb
```

##  Dataset

[Real Market Data for Association Rules](https://www.kaggle.com/datasets/rukenmissonnier/real-market-data)
