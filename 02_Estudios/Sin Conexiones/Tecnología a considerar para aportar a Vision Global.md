Tecnología a considerar:

1. Procesador: **AMD EPYC Serie 9005** y **Intel Xeon Scalable (Generaciones 4 y 5)**  - Posible
2. Tarjeta gráfica para la IA: **NVIDIA MGX y la Serie L40S** - Posible la tarjeta, la serie muy cara
3. Para almacenamiento de datos: **Tecnología NVMe Enterprise** - Posible
4. Para conectarse con Robots a buscar datos: **UiPath Automation Suite** - 420 mes caro
5. Terminal Bloomberg pero Open Source: **OpenBB Terminal** - Gratis, peor fuente de precios no incluida - Posible
6. Modelo LLM: **FinGPT** - Se puede usar en un servidor, pero se necesita tarjeta. Hay opciones en internet, pero no funcionan hay que averiguar.
7. Arquitectura de datos: **Data Lakehouse** a traves de Apache Hudi, Dremio o Ilum
8. Almacenamiento: **MinIO** - Es posible que no lo necesitemos
9. Motor de consultas: **Trino o StarRocks** - Posible conexion a SQL Server para mejorarlo
10. Orquestador de datos: **Prefect**
11. Para análisis: **Metabase**



Para entender:

Prefect se encarga de que las tareas ocurran en la secuencia correcta. Por ejemplo:

- **Paso 1:** El robot de **UiPath** busca datos financieros.
- **Paso 2:** Solo cuando el robot termina, se guardan los archivos en **MinIO**.
- **Paso 3:** Una vez guardados, **FinGPT** lee esos archivos para analizarlos.
- **Paso 4:** Los resultados se envían a **StarRocks** para que los veas en **Metabase**.