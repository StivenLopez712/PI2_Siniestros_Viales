**<p align="center">PROYECTO INDIVIDUAL 2</p>**
**<p align="center">SINIESTROS VIALES CON VÍCTIMAS FATALES EN CABA (2016-2021)</p>**


El objetivo principal del proyecto consiste en generar información putil para las autoridades locales, con el fin de tomar mejores medidas dirigidas a reducir la cantidad de victimas fatales en los siniestros viales en CABA,  el proyecto se realiza en base a informacion dada por el gobierno de Argentina, informacion coprendida entre 2016 y 2021.

El proyecto se llevó a cabo usando Python, pandas, matplotlib, seaborn, entre otras y power BI. Se realizó un ETL para realizar la limpieza de los datos, seguido de un análisis exploratorio que ayuda a sacar conclusiones y observar las estadisticas de los datos limpiios.

**DATOS**
Durante el pryecto, se utilizó la Base de Víctimas Fatales en Siniestros Viales del gobierno de Argentina, la cual está en excel y consta de dos pestañas de datos:

- HECHOS: Esta pestaña incluye una fila por cada incidente con un identificador único y variables relacionadas con el tiempo, el espacio y los participantes asociados a ese incidente.

-VICTIMAS: En esta pestaña, cada fila representa a una víctima de los incidentes y contiene información sobre la edad, sexo y modo de desplazamiento asociados a cada víctima. Estos datos se conectan a los incidentes a través del identificador único de cada incidente en la pestaña HECHOS.


**ETL y EDA**

En esta etapa se buscaron y detectaron valores faltantes, nulos y repetidos, se rellenaron y completaron datos en algunos casos, y se eliminaron completamente en otros. Se eliminaron algunas columnas que no se usarian para disminuir el tamaño del dataset, por ejemplo, eliminación de la columna "Altura", considerada no relevante.

Todo el proceso de ETL llevó a cabo de forma local utilizando Visual Studio Code (VSCODE). Se utilizó Jupyter Notebook como el entorno principal, y Python respaldado por bibliotecas como numpy y pandas para manipular los datos de manera eficiente. Este método aseguró un flujo de trabajo organizado y coherente, facilitando un desarrollo eficiente del proyecto.


Después de completar el proceso ETL y obtener los datos resultantes, se llevó a cabo un análisis exploratorio de datos (EDA) que reveló tendencias y patrones en algunos datos. Este análisis se amplió para incluir un examen detallado tanto en términos temporales como geográficos después de la ejecución del ETL. Se exploraron las variaciones en el número de víctimas a lo largo de los años y se examinaron los incidentes viales en las diversas comunas de CABA. Este análisis proporcionó patrones sobre las calles con mayores riesgos y los posibles factores que influyen en la cantidad de fatalidades en accidentes de tráfico. Además, se abordaron aspectos como el tipo de víctima y la relación entre el tipo de vehículo involucrado y los presuntos responsables.

De esta manera se detectaron patrones importantes, por ejemplo, a lo largo de los años, la gran mayoria de victimas son de sexo masculino, el vehiculo mas involucrado como victima es Moto, los cruces y avenidas son las zonas con mayor riesgo y con mayor registro de accidentes, entre otras tendencias que se pueden ver en el notebook.

Todos los análisis con sus gráficas se encuentran en el NoteBook ETL_EDA.


**Indicadores KPI:**
Para este proyecto, se desarrolaron 3 kpi's, dos ya planteados y un tercero planteado por  cuenta propia:

Primer KPI:
'Reducir 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior'

Dónde, definimos a la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales(HSV) / Población total) * 100,000

El KPI1 se cumple solamente en 4 semestres, correspondientes a: los dos semestres del 2019, primer semestre del 2020 y segundo semestre del 2021.

Probablemente la disminucion en estos años esté estrechamente relacionada con la masiva disminucion de tráfico a nivel mundial como consecuencia de la pandemia.

Segundo KPI:
Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.

Para el segunfo KPI, definimos a la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

Se observó que se cumple este KPI en 2017,2019 y 2020, en los demás años hubo incremento en las accidentes mortales para motociclistas con excepcion de 2018. En los años de Pandemia 2019-2020 se observa una disminucion de accidentes, sin embargo en 2021 se nota una tendencia considerable en el aumento de este tipo de hechos. puede deberse al retorno paulatino de la movilidad en el mundo y al incremento del uso de motocicletas como medio de transporte, derivado tambien de la pandemia (mucha gente empezó a trabajar como repatidor y similares).

Tercer KPI:
Reducir la cantidad de accidentes mortales en los Cruces en un 5% respecto al año anterior:

Definimos este KPI cómo (cantidad de victimas en cruces el año anterior - cantidad de victimas en cruces este año)/(cantidad de victimas en cruces el año anterior)*100

Se observó que el KPI no se pudo cumplir en ninguno de los años, esto es un dato interesante y de importancia, pues llama a las autoridades a tomar acción lo antes posible en este tipo de zonas, es necesario implementar medidas que aseguren una disminucion de este tipo de acontecimientos, por ejemplo, colocar reductores de velocidad, mayor señalizacion o semaforos. 

**Dashboard**

Con la ayuda de Power BI se desarrolló un dashboard interactivo que nos permite ver de mejor manera las diferentes métricas y como estas varian durante los años, o tambien, segun el tipo de victima,acusado, dia de la semana, entre otros, POWER BI es una gran herramienta que permite ver de forma facil y condensada toda la extensa informacion que se adquirió durante el proceso de limpieza y análisis de los datos provistos.


**Conclusiones**

- Se observó una notable reducción en la tasa de homicidios en siniestros viales durante los años 2019 y 2021, cumpliendo con el primer KPI establecido. Estos períodos destacan por alcanzar y superar la meta del 10%, posiblemente relacionada con la disminución del tráfico global durante la pandemia.

- A pesar de cumplir el segundo KPI en algunos años, se destaca una tendencia al alza en los accidentes mortales de motociclistas, especialmente en 2021. Este aumento puede vincularse al retorno gradual de la movilidad y al incremento del uso de motocicletas como medio de transporte durante la pandemia.

- El proceso ETL y el análisis exploratorio revelan patrones importantes, como la mayoría de víctimas siendo de sexo masculino, la prevalencia de motos como vehículos involucrados y la identificación de zonas de mayor riesgo. Estos hallazgos respaldan la utilidad de estas etapas en la generación de información valiosa.