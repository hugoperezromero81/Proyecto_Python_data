# 📊 Proyecto de Análisis de Datos -- Marketing Bancario & Clientes

## 🗂️ Estructura del proyecto

    Proyecto_Python_Data/
    │
    ├── data/
    │   ├── Archivos_origen/        # 📥 Archivos en bruto (originales: .csv, .xlsx)
    │   ├── Archivos_limpios/       # 🧹 Archivos después del proceso de limpieza
    │   ├── Doc_proyecto/           # 📜 Archivos después del proceso de limpieza
    │
    ├── notebooks/
    │   ├── 01_Analisis_preliminar.ipynb   # 🔍 Análisis inicial de columnas
    │   ├── 02_Limpieza_datos.ipynb        # 🧽 Proceso de limpieza completo
    │   ├── 03_EDA_exploratorio.ipynb      # 📊 Exploración y visualización de datos
    │
    ├── src/                       # ⚙️ (opcional) Funciones auxiliares reutilizables
    │
    └── README.md                  # 📑 Documentación principal del proyecto

------------------------------------------------------------------------

## 📚 Librerías utilizadas

-   **Pandas** 🐼 → Manejo y limpieza de datos tabulares\
-   **NumPy** 🔢 → Cálculos numéricos y estadísticos\
-   **Matplotlib** 📈 → Visualización básica de gráficos\
-   **Seaborn** 🎨 → Visualización avanzada y estilizada\
-   **os** 📂 → Manejo de rutas y archivos del sistema\
-   **dateparser** ⏳ → Procesamiento flexible de fechas (fase de
    limpieza)

    ------------------------------------------------------------------------

## 🧭 Flujo del proyecto

### 1️⃣ Análisis preliminar (`01_Analisis_preliminar.ipynb`)

-   Revisión de **tipos de variables** (numéricas, categóricas,
    fechas).\
-   Obtención de estadísticas descriptivas (`count`, `mean`, `std`,
    etc.).\
-   Identificación de **valores atípicos** y **moda en categóricas**.

📌 *Objetivo:* detectar problemas iniciales antes de limpiar.

------------------------------------------------------------------------

### 2️⃣ Limpieza de datos (`02_Limpieza_datos.ipynb`)

-   🔄 **Unificación de hojas** del Excel de clientes en un solo
    DataFrame.\
-   🧹 Tratamiento de valores **`unknown`** y **nulos**.\
-   📅 Creación de **variables derivadas de fechas** (antigüedad
    cliente).\
-   🚨 Detección y tratamiento de **outliers**.\
-   🔤 Normalización de texto en variables categóricas.\
-   🔑 Conservación de la columna **`id`** para unir los datasets.\
-   💾 Exportación de archivos limpios:
    -   `customer-details_limpio.xlsx`\
    -   `bank-additional_limpio.xlsx`

📌 *Objetivo:* generar datasets homogéneos y consistentes para análisis.

------------------------------------------------------------------------

### 3️⃣ Análisis Exploratorio (EDA) (`03_EDA_exploratorio.ipynb`)

#### 🔹 **Bloque 1 -- Bank**

1.1 Distribución de edades y aceptación de campaña 👩‍🦳🧑‍💼\
1.2 Nivel educativo y aceptación 🎓\
1.3 Profesión y aceptación 💼\
1.4 Estado civil y aceptación 💍

#### 🔹 **Bloque 2 -- Variables de campaña**

2.1 Canal de contacto (móvil vs. fijo) 📞\
2.2 Duración de llamada y aceptación ⏱️\
2.3 Número de contactos en campaña 🔢\
2.4 Información de campañas anteriores 📜

#### 🔹 **Bloque 3 -- Customer**

3.1 Distribución de ingresos 💰\
3.2 Composición familiar (niños/adolecentes en el hogar) 👨‍👩‍👧‍👦\
3.3 Análisis de visitas web 🌐

#### 🔹 **Bloque 4 -- Combinado**

4.1 Ingresos vs aceptación 💰➡️✅\
4.2 Tamaño del hogar vs aceptación 👪➡️✅\
4.3 Canal de contacto vs aceptación ☎️➡️✅\
4.4 Ingresos + profesión vs aceptación 📊

📌 *Objetivo:* identificar patrones y factores más influyentes en la
respuesta positiva de campañas.

------------------------------------------------------------------------

## 📝 Tipo de código utilizado

-   **EDA estructurado y comentado** → cada bloque contiene:
    -   Código de cálculo (`groupby`, `value_counts`, `describe`).\
    -   Gráficos 📊 (barras, distribuciones, stacked bars).\
    -   Tablas resumen con proporciones (%).\
    -   Explicación en **Markdown** con hallazgos.
-   **Estilo reproducible**:
    -   Variables y gráficos homogéneos.\
    -   Bloques numerados (1, 1.1, 1.2 ...).\
    -   `display()` para mejor presentación de tablas.\
    -   Colores consistentes (`colormap="coolwarm"`,
        `seaborn whitegrid`).

------------------------------------------------------------------------

## 📌 Conclusiones clave del análisis

-   👩‍💼 **Edad y educación** influyen en la aceptación: grupos jóvenes
    con mayor formación muestran tasas más altas.\
-   📞 **Canal de contacto** es determinante: llamadas móviles resultan
    más efectivas que fijos.\
-   📜 **Historial de campañas** previo condiciona la respuesta actual.\
-   💰 **Ingresos + profesión** permiten identificar perfiles
    prioritarios para futuras campañas.\
-   👪 **Tamaño del hogar** tiene relación con las decisiones de
    aceptación.

------------------------------------------------------------------------

## 🚀 Próximos pasos

-   Crear un modelo de predicción (**Machine Learning**) basado en las
    variables más relevantes.\
-   Optimizar la segmentación de clientes para campañas futuras.\
-   Desarrollar visualizaciones interactivas con **Power BI o Tableau**.

------------------------------------------------------------------------

## Autor

- Creado por: **Hugo Pérez**
