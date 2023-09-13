# Predicción de Precios de Bienes Raices en Australia - Regresión Avanzada

## Índice

- [Índice](#índice)
- [Introducción](#introducción)
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo Comercial](#objetivo-comercial)
  - [Preparación de Datos:](#preparación-de-datos)
  - [Construcción y Evaluación del Modelo](#construcción-y-evaluación-del-modelo)
  - [Conclusiones](#conclusiones)
    - [Regresión Ridge](#regresión-ridge)
    - [Regresión Lasso](#regresión-lasso)
    - [Regresión ElasticNet](#regresión-lasso)
    - [Las Variables Más Significativas Son:](#las-variables-más-significativas-son)

## Introducción

Se aplica regresión utilizando la regularización para predecir el valor real de las posibles propiedades

### Métodos Utilizados
* Analisis EDA
* Limpieza de datos(inputacion de valores nulos)
* Estandarizacion
* OneHotEncoding
* Analisis de correlacion de Pearson

### Tecnologías
* Python
* Pandas
...

## Descarga y Configuración
### Requisitos Previos

Este proyecto necesita que Anaconda esté instalado en la computadora.

Para más detalles sobre la instalación, visite: https://docs.anaconda.com/anaconda/install/index.html

### Cómo Ejecutar

Puede descargar el código fuente clonando este repositorio usando Git:

1. Abra su aplicación Terminal favorita (Unix, Linux o Macos), como Terminal, Comando, Consola, iTerm2, etc.

2. Clone el repositorio

```
git clone <GITHUB_REPO_URL>
```

3. Abra el archivo notebook ** *.ipynb** en Anaconda.

```
jupyter notebook <FILE.ipynb
```


## Declaración del Problema

Una empresa de vivienda con sede en EE. UU. llamada Surprise Housing ha decidido ingresar al mercado australiano. La empresa utiliza el análisis de datos para comprar casas a un precio inferior a sus valores reales y venderlas a un precio más alto. Con el mismo propósito, la empresa ha recopilado un conjunto de datos de la venta de casas en Australia. Los datos se proporcionan en el archivo CSV a continuación.

La compañía está buscando posibles propiedades para comprar e ingresar al mercado.

### Objetivo Comercial

Construir un modelo de regresión utilizando la regularización para predecir el valor real de las posibles propiedades y decidir si invertir en ellas o no


### Preparación de Datos:

1. Limpieza de Datos y Análisis de Datos Faltantes.
2. Análisis y Tratamiento de Valores Atípicos.
3. Derivación de Columnas Categóricas.
4. Análisis Univariable.
5. Análisis Bivariable.


### Construcción y Evaluación del Modelo

1. División de datos de entrenamiento y prueba.
2. Escalado de Características - StandardScaler.
3. Ingeniería y Selección de Características usando RFE y el Factor de Inflación de Varianza.
4. Preparación del modelo usando OLS & Regresión Lineal.
5. Modelos de Regularización Ridge, Lasso y ElasticNet.
6. Análisis de Residuos.
7. Evaluación y Valoración del Modelo.
8. Predicción.
9. Conclusión y Análisis Final.

### Conclusiones
* El modelo ganador se obtiene aplicando regularizacion con ElasticNet con un rmse de 0.2955879198293417, aunque Ridge se acaerca muchisimo con un valor de 0.2958049829870227

### Conclusions

R2_Score for Ridge regresion.... 
R2_Score for Lasso regresion.... 
R2_Score for ElasticNet regresion.... 

#### Ridge Regression
* **Optimal Lambda Value:** 8.214343584919423
* **R2 Score Train:** 0.9377710322566428
* **R2 Test Score:**  0.9120325672950937
* **RMSE Test:**      0.2958049829870227

#### Lasso Regression
* **Optimal Lambda Value:** 0.0013200884008314193
* **R2 Score Train:**  0.8143154815533686
* **R2 Test Score:**   0.8235767395077397
* **RMSE Test:**       0.41891166023504395

#### ElasticNet Regression
* **Optimal Lambda Value:** 0.0013200884008314193
* **R2 Score Train:**  0.933302144863126
* **R2 Test Score:**   0.9121616218005872
* **RMSE Test:**       0.2955879198293417

#### Las Variables Más Significativas Son:
* 2 LotArea	0.05
* 3	OverallQual	0.36
* 5	YearBuilt	0.10
* 6	YearRemodAdd	0.05
* 8	BsmtFinSF1	0.06
* 11	TotalBsmtSF	0.09
* 15	GrLivArea	0.25
* 23	Fireplaces	0.01
* 25	GarageCars	0.04
* 26	GarageArea	0.03
