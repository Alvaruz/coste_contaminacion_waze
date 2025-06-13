# Análisis de Coste de Contaminación y Congestión con Waze

## Descripción
Este proyecto analiza y calcula el coste operativo de congestión y el impacto ambiental utilizando datos de tráfico proporcionados por Waze. El análisis se enfoca en cuantificar el impacto económico y ambiental de la congestión vehicular en términos monetarios (guaraníes).

## Centro Avanzado de Gestión del Tráfico (ATMS)
Proyecto desarrollado para el Centro Avanzado de Gestión del Tráfico, con el objetivo de proporcionar herramientas de análisis de datos para la toma de decisiones en la gestión del tráfico urbano.

## Contenido del Repositorio

### Notebook Principal
- [`calculo.ipynb`](calculo.ipynb): Notebook Jupyter con el análisis detallado de los costes operativos y emisiones.

### Datos de Referencia
- `tabla_velocidad_emisiones_costeoperativo.csv`: Tabla de referencia con datos de velocidad, emisiones y costes operativos.
- `tabla_resumen_calculo_convencional.csv`: Tabla de resumen para comparar con cálculos convencionales.
- `waze_postgres.md`: Documentación sobre la estructura de la base de datos PostgreSQL utilizada con datos de Waze.

## Metodología
El análisis se basa en datos de Waze, donde se extraen registros de congestión (jams) y se calculan diversos indicadores:

1. **Datos base por hora del día**:
   - Velocidad promedio (km/h)
   - Longitud promedio de tramos (km)
   - Vehículos promedio por tramo
   - Número de registros Waze

2. **Cálculos económicos**:
   - Coste operativo por vehículo
   - Coste operativo total por tramo
   - Emisiones por vehículo
   - Costo total de emisiones por tramo

3. **Visualizaciones**:
   - Gráficos de barras por hora del día
   - Comparativas entre costes operativos y emisiones
   - Correlaciones entre variables
   - Patrones de congestión diaria

## Requisitos
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SQLAlchemy (para conexión a PostgreSQL)
- Psycopg2
- Python-dotenv
- Openpyxl (para exportar a Excel)

## Uso
1. Configure las credenciales de la base de datos en un archivo `.env`.
2. Ejecute el notebook `calculo.ipynb`.
3. Explore las visualizaciones y análisis generados.

## Resultados Clave
- Identificación de horas pico de congestión: 7-9h y 17-19h.
- Cuantificación del coste económico de la congestión por hora.
- Proporción entre costes operativos (~90%) y emisiones (~10%).
- Correlación entre velocidad y costes totales.
- Comparativa con métodos convencionales de cálculo.

## Conexión con Base de Datos
El proyecto se conecta a una base de datos PostgreSQL que almacena datos históricos de congestión de Waze. La estructura de los datos incluye campos como jam_speed, jam_length, delay_seconds, entre otros indicadores relevantes del tráfico.

---

*Proyecto desarrollado para el Centro Avanzado de Gestión del Tráfico (ATMS)*
