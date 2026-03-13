# Visualización cifras de presuntos suicidios del 2015 al 2023

[**➔ Ver en Google Colab**](https://colab.research.google.com/github/AndrewP05/Visualizacion_Cifras_Suicidios/blob/main/Visualizacion.ipynb)

## Descripcion datos
El presente analisis tiene como fuente dos bases de datos tomadas de la pagina [**Datos Abiertos Colombia**](https://https://www.datos.gov.co/) que nos ayudaran a visualizar la información prevalente de los presuntos suicidios ocurridos en el territorio nacional Colombiano en el periodo de tiempo comprendido entre los años 2015 a 2023 de los cuales tiene conocimiento y son registrados por el Instituto Nacional de Medicina Legal y Ciencias Forenses.


#### DB - Presuntos Suicidios colombia del 2015 a 2023


*   Ultima Actualizacion: 5 de diciembre de 2024
*   Fuente: [PRESUNTOS SUICIDIOS COLOMBIA DEL 2015 A 2023](https://www.datos.gov.co/Justicia-y-Derecho/Presuntos-Suicidios-Colombia-2015-a-2023-Cifras-de/f75u-mirk/about_data)
*   Diccionario de datos: Tenemos **23500** filas y **35** Columnas con:

| Nombre de la columna | Descripción | Tipo de dato               |
|----------------------|-------------|----------------------------|
| `id`              |  Numeración secuencial en el sistema con respecto al registro de los casos            | Texto                                    |
| `a_o_del_hecho`            | Rango de tiempo en el que se dieron los hechos, se encuentra establecido por el período que transcurre desde el día 1 de enero hasta el 31 de diciembre | Texto        |
| `grupo_de_edad_de_la_victima`           | Tiempo que ha vivido una persona u otro ser vivo contando desde su nacimiento hasta su fallecimiento, capturado en un intervalo de tiempo     |  Texto                 |
| `grupo_mayor_menor_de_edad`         | Agrupación de casos según se trate de víctimas mayores o menores de edad      | Texto                |
| `edad_judicial`           | Agrupacion de casos en rangos de edades que son de interés judicial  | Texto                |
| `ciclo_vital`              | Corresponde al establecimiento de la etapa de desarrollo vital en que se encontraba la víctima, al momento del fallecimiento            | Texto                                    |
| `sexo_de_la_victima`             | 	Se refiere a la variable biológica que clasifica a la población en hombres y mujeres               |   Texto                  |
| `estado_civil`            | Es la situación de cada persona en relación con las leyes o costumbres relativas al matrimonio que existen en el país  |  Texto               |
| `pais_de_nacimiento_de_la_victima`           | Lugar de nacimiento registrado en el documento de identidad   | Texto                 |
| `escolaridad`                 | 	Se refiere al grado de escolaridad más alto al cual ha llegado la persona de acuerdo con los niveles del sistema educativo formal: preescolar, básica en sus niveles de primaria, secundaria, media y superior            |  Texto                  |
| `pertenencia_grupal`          | 	Se entienden como las características de las personas o grupos sociales, que los hacen más frágiles o susceptibles para enfrentar los riesgos, lo que hace que la probabilidad de la ocurrencia de la violencia y de la afectación sea mayor que en cualquier otra persona               |  	Texto                  |
| `mes_del_hecho`       | 	Tiempo determinado por el mes en el cuál se establece el momento en que ocurrieron los hechos            |  	Texto                  |
| `dia_del_hecho`           | 	Día de la semana en la que ocurrió el hecho                 |  Texto                  |
|`rango_de_hora_del_hecho_x_3_horas`| Intervalo de tiempo o categoría cronológica, en el cual se establece que sucedieron los hechos| Texto |
|`codigo_dane_municipio`|División Político Administrativa (DIVIPOLA). Es una codificación estándar, numérica, que identifica a las entidades territoriales dándole a cada municipio, una identidad única, inconfundible y homogénea|Texto|
|`municipio_del_hecho_dane`|	Entidad territorial fundamental de la división político-administrativa del Estado colombiano, donde ocurrieron los hechos|Texto|
|`departamento_del_hecho_dane`|Para Colombia: Entidad territorial de primer nivel de la división político-administrativa del Estado que agrupa municipios y áreas no municipalizadas (departamento), donde ocurrieron los hechos|Texto|
|`codigo_dane_departamento`|División Político Administrativa (DIVIPOLA). Es una codificación estándar, numérica, que identifica a las entidades territoriales dándole a cada departamento, una identidad única, inconfundible y homogénea|Texto|
|`escenario_del_hecho`|Clasificación del lugar donde ocurrieron los hechos|Texto|
|`zona_del_hecho`|Clasificación del territorio que diferencia los espacios comprendidos dentro del casco urbano de un municipio y los centros poblados (zona urbana), de los que están fuera de él (zona rural)|Texto|
|`actividad_durante_el_hecho`|Clasificación de las tareas u operaciones que se encontraba realizando la persona en el momento de los hechos|Texto|
|`circunstancia_del_hecho`|	Establece una relación entre la víctima y la situación del entorno en el momento de los hechos|Texto|
|`manera_de_muerte`|Se establece la manera o tipo de muerte, de acuerdo a la evaluación de la hipótesis e información aportada por la autoridad judicial que atiende el caso|Texto|
|`mecanismo_causal`|	Se clasifican los casos de muerte de acuerdo a la causa principal que la originó, pueden ser por enfermedad y también por algún tipo de trauma o lesión externa.|Texto|
|`diagnostico_topografico_de_la_lesion`|Zona anatómica general establecida por la necropsia, donde se produjo la lesión|Texto|
|`presunto_agresor`|Caracterización de la persona que se presume, o se sabe, ha sido el causante de la muerte|Texto|
|`condicion_de_la_victima`|Clasificación del rol de la víctima según la forma del desplazamiento en el momento del evento|Texto|
|`medio_de_desplazamiento_o_transporte`|Medio de desplazamiento utilizado por la víctima en el momento del evento. No aplica para el peatón.|Texto|
|`servicio_del_vehiculo`|Tipo de servicio que presta el medio de desplazamiento en el que se movilizaba la víctima al momento del evento de transporte. No aplica para el peatón|Texto|
|`clase_o_tipo_de_accidente`|Es cualquier tipo de evento que involucra a un medio diseñado fundamentalmente para llevar personas o bienes de un lugar a otro, o usado primordialmente para ese fin en el momento del evento|Texto|
|`objeto_de_colision`|Objeto contra el cual choca el medio de desplazamiento en el que se transportaba la víctima al momento del evento de transporte|Texto|
|`servicio_del_objeto_de_colision`|Tipo de servicio que presta el objeto de colisión contra el que choca el medio de desplazamiento en el que se movilizaba la víctima al momento del evento de transporte|Texto|
|`razon_del_suicidio`|Razón o causa principal a la que se le atribuye el acto del suicidio cometido|Texto|
|`localidad_del_hecho`|	Localidad / Comuna: se denomina Localidad o Comuna a una unidad administrativa de una ciudad media o principal del país que agrupa sectores o barrios determinados|Texto|
|`ancestro_racial`|	Descendencia de cada uno de los grandes grupos étnicos en que se suele dividir la especie humana, teniendo en cuenta ciertas características físicas distintivas|Texto|

## Objetivos

### General

1. Analizar y visualizar de manera integral las tendencias y características de los presuntos suicidios ocurridos en Colombia entre 2015 y 2023, con el fin de identificar patrones temporales, demográficos y geográficos que aporten información útil para el diseño de estrategias de prevención y atención.

### Especificos

1. Determinar la variación anual del número de casos de presuntos suicidios y elaborar gráficas para observar picos, valles y tendencias generales.
2. Analizar la distribución por sexo, grupo de edad, estado civil y nivel de escolaridad, para identificar poblaciones con mayor incidencia.
3. Visualizar la frecuencia de casos por departamento y municipio, diferenciando zona urbana y rural, para localizar hotspots y regiones con concentraciones significativas.

# Gráfica 1: Suicidios por año y sexo

<img width="1184" height="584" alt="image" src="https://github.com/user-attachments/assets/b8dd1ee2-62c7-4b6c-9cab-85fa9a5cf649" />
Se observa que los hombres representan consistentemente la mayoría de los casos de suicidio en todos los años del período analizado. Aunque hay variaciones leves año a año, la tendencia de mayor prevalencia en hombres se mantiene. Esto sugiere la necesidad de estrategias de salud mental diferenciadas por género, con especial atención al grupo masculino.

# Gráfica 2: Ciclo vital más afectado

<img width="1184" height="583" alt="image" src="https://github.com/user-attachments/assets/d029da99-a2fe-46d2-9c45-b7eed8b3cc42" />
Los suicidios se concentran principalmente en las etapas de la juventud y adultez, con una participación menor de la niñez y la vejez. Esto puede estar asociado a factores como presión académica, dificultades laborales, relaciones personales o problemas económicos, que suelen afectar a estas etapas de forma más crítica.

# Gráfica 3: Razones más frecuentes de suicidio (top 10)

<img width="1184" height="584" alt="image" src="https://github.com/user-attachments/assets/85821ecf-8f2b-4ec5-a486-3f4525fb99e7" />
Entre las principales razones reportadas se destacan problemas afectivos, familiares y de salud mental. La presencia de causas como depresión y conflictos interpersonales revela la importancia de mejorar la cobertura, detección temprana y seguimiento en servicios de salud mental.

# Gráfica 4: Relación entre grupo de edad y sexo

<img width="1184" height="583" alt="image" src="https://github.com/user-attachments/assets/11feafa5-a7d2-43a2-941f-a966c8ef751a" />
En los grupos de edad más jóvenes y adultos (20 a 39 años), los hombres presentan una mayor incidencia que las mujeres. Sin embargo, en adolescentes también se nota una participación significativa de mujeres. Esto indica que las estrategias de prevención deben tener un enfoque diferencial por sexo y etapa de desarrollo.

# Gráfica 5: Suicidios por nivel educativo (top 8)

<img width="1184" height="583" alt="image" src="https://github.com/user-attachments/assets/4c14f1f7-da92-4cf7-83cc-f479aaea2903" />
Los casos de suicidio se presentan con mayor frecuencia en personas con educación básica y media, aunque también hay un número importante en quienes no registran nivel educativo. Este patrón podría estar relacionado con limitaciones socioeconómicas, desempleo o acceso restringido a oportunidades, factores que influyen en la salud mental.

# Grafica 6: Distribución de razones del suicidio por grupo de edad

<img width="1373" height="684" alt="image" src="https://github.com/user-attachments/assets/7262d0d9-c3ed-48e8-8dc3-f31ed1298c14" />
El gráfico muestra que las razones del suicidio varían significativamente según el grupo de edad, reflejando cómo las preocupaciones emocionales, familiares y de salud cambian a lo largo del ciclo vital. En los jóvenes predominan los problemas afectivos y familiares, mientras que en adultos mayores se hacen más visibles las razones asociadas a la salud física y mental. Esta distribución evidencia la necesidad de estrategias de prevención del suicidio con enfoques diferenciados, que respondan a las problemáticas específicas de cada etapa de la vida.

# Conclusion general del estudio
Los datos muestran que el suicidio en Colombia afecta principalmente a hombres jóvenes y adultos, con factores como problemas afectivos, familiares y mentales como causas principales. La concentración en ciertos niveles educativos y ciclos vitales sugiere que los programas de prevención deben tener un enfoque integral, dirigido especialmente a estas poblaciones vulnerables. Además, se evidencia la necesidad de fortalecer la educación emocional y el acceso oportuno a servicios de salud mental, especialmente en contextos escolares, laborales y comunitarios.
