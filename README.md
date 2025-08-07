# Challenge-Telecom-X---Parte-2


## 🎯 Propósito del análisis
Este proyecto tiene como objetivo **predecir la cancelación (churn)** de clientes de una compañía de telecomunicaciones a partir de variables relevantes.  
Con este análisis buscamos **identificar patrones y factores de riesgo** que ayuden a la empresa a implementar estrategias para **reducir la fuga de clientes** 💡.

## 📂 Estructura del proyecto
TelecomX-Parte2/
│
├── data/
│ ├── data_telecom_x2.csv # Datos tratados y listos para modelar
│
├── notebooks/
│ ├── DesafioTelecom.ipynb # Cuaderno principal del análisis
│
├── visuals/
│ ├── correlaciones.png # Mapa de calor de correlaciones
│ ├── distribucion_churn.png # Distribución de clientes churn/no churn
│
├── README.md
└── requirements.txt # Librerías necesarias


## 🛠️ Proceso de preparación de datos

### 1️⃣ Limpieza y selección de variables
- Eliminación de columnas irrelevantes: `id`, `meses_de_contrato`, `cuentas_diarias` 🗑️.
- Verificación de la proporción de cancelación para identificar posible **desbalance de clases**.

### 2️⃣ Clasificación de variables
- **Categóricas**: `genero`, `servicio_internet`, `tipo_contrato`, `metodo_pago`, etc.
- **Numéricas**: cargos mensuales, cargos totales, etc.

### 3️⃣ Codificación de variables
- Transformación manual de categorías a valores numéricos:
  - `genero`: male → 0, female → 1
  - `servicio_internet`: fiber optic → 0, dsl → 1, no → 2
  - `tipo_contrato`: month-to-month → 0, two year → 1, one year → 2
  - `metodo_pago`: electronic check → 0, mailed check → 1, bank transfer (automatic) → 2, credit card (automatic) → 3

### 4️⃣ División de datos
- 70% para **entrenamiento** y 30% para **prueba** usando `train_test_split` ✂️.

## 🤖 Modelización y decisiones
- Algoritmos probados: **Regresión Logística**, **Random Forest**, **XGBoost**.
- Se priorizó **Random Forest** por su mejor rendimiento en *recall*, minimizando falsos negativos (clientes que se van y el modelo no detecta) 🚨.

---

## 📊 EDA – Análisis Exploratorio de Datos
Durante la exploración se generaron gráficos para entender mejor los datos:

**Mapa de calor de correlaciones** 🔥  
![Mapa de calor](visuals/correlaciones.png)

**Distribución de clientes churn/no churn** 📉  
![Distribución churn](visuals/distribucion_churn.png)

**Insight clave:** Los clientes con contrato mensual y pagos electrónicos automáticos presentan mayor tasa de cancelación, especialmente cuando los cargos mensuales son altos.


## ▶️ Instrucciones de ejecución

1. **Clonar el repositorio**
2. **Instalar dependencias**
   pip install -r requirements.txt
3.**Ubicar datos**
4. **Ejecutar cuaderno**

## **AUTOR**
**aNA bANANA**
