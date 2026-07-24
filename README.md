# analysis-ConnectaTel
ConnectaTel Customer Analysis – Sprint 7

Este repositorio contiene el análisis realizado durante el Sprint 7 del caso ConnectaTel, empresa de telecomunicaciones en Latinoamérica.

El análisis utiliza tres datasets (plans, users_latam, usage) con información registrada hasta el año 2024, e incluye valores nulos, sentinels y outliers que simulan problemas reales de calidad de datos.

📂 Contenido del repositorio
S7_Version-Estudiante-Project-ConnectaTel.ipynb → Notebook principal con limpieza, EDA, distribuciones, outliers, segmentación de clientes y conclusiones.
datasets/ → Carpeta con los archivos plans.csv, users_latam.csv y usage.csv.
▶ Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asalasiniguez-a20s/analysis-ConnectaTel/blob/main/S7_Version_Estudiante_Project_ConnectaTel.ipynb)

O:

Abre el archivo .ipynb en GitHub.
Haz clic en Open in Colab.
⚙️ Requisitos
Python 3.9 o superior
Librerías: pandas, numpy, matplotlib, seaborn

Instalación rápida:

bash
pip install pandas numpy matplotlib seaborn

📘 Cómo reproducir el análisis
- Abre S7_Version-Estudiante-Project-ConnectaTel.ipynb.

- Sube los archivos plans.csv, users_latam.csv y usage.csv a la carpeta /datasets/ (en Colab puedes usar files.upload() si no vienen precargados en el entorno).

- Ejecuta las celdas en orden, ya que los pasos posteriores dependen de las tablas construidas en pasos anteriores (ej. user_profile).

- Revisa los bloques de markdown (💡 Insights y ✍️ Comentarios) donde se documentan las decisiones de limpieza y los hallazgos de cada etapa.


🧠 Objetivo del análisis
- Identificar problemas de calidad de datos (nulos, sentinels, fechas inválidas).

- Construir un perfil de uso por usuario a partir de los registros de actividad.

- Analizar comportamientos, distribuciones y outliers en variables de uso (mensajes, llamadas, minutos) y demográficas (edad).

- Segmentar a los clientes por nivel de uso y grupo de edad.

- Generar insights accionables para el equipo comercial de ConnectaTel (campañas de fidelización, promoción de planes, ofertas personalizadas).


🗂️ Datasets
Archivo	Descripción

- plans.csv	Precio, minutos y GB incluidos, costo por extra de cada plan.

- users_latam.csv	Edad, ciudad, plan contratado, fecha de registro y de cancelación por usuario.

- usage.csv	Eventos de llamada/mensaje por usuario: tipo, duración, longitud y fecha.


🧩 Etapas del análisis
- Carga y exploración inicial de los tres datasets.

- Identificación de nulos, sentinels (-999 en age, ? en city) y fechas fuera de rango.

- Limpieza: imputación de age con la mediana, city a NA, fechas inválidas a NaT.

- Agregación de usage por usuario y construcción de user_profile.

- Visualización de distribuciones (histogramas) y detección de outliers (boxplots, método IQR).

- Segmentación de clientes por grupo_uso (Bajo/Medio/Alto) y grupo_edad (Joven/Adulto/Adulto Mayor).

- Insight ejecutivo con hallazgos y recomendaciones comerciales.
