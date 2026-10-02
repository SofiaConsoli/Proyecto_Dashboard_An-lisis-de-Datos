# Proyecto_Dashboard_Análisis_de_Datos
Repositorio creado con el fin de realizar la entrega del proyecto de lógica de Katas del módulo de Dashboard &amp; Análisis de Datos del bootcamp de Data And Analytics de la escuela ThePower Education. URL Google Sheet donde se encuentra el trabajo: https://docs.google.com/spreadsheets/d/14IcrGtQiVIWxLqw2jn3YSpS6Ux7fImlUb1DU7fVYtlw/edit?usp=sharing .

1. Introducción							
							
El presente proyecto tiene como objetivo realizar un análisis exploratorio de un conjunto de datos relacionado con las características demográficas, educativas y laborales de una población adulta, así como estudiar su relación con el nivel de ingresos.							
							
Para ello, se ha utilizado un dataset compuesto inicialmente por 48.842 registros y 15 variables. A partir de los datos originales se realizó un proceso de limpieza y transformación, seguido de un análisis descriptivo mediante tablas dinámicas y gráficos. El mismo fue obtenido de la siguiente fuente: https://www.kaggle.com/datasets/mastmustu/income/data .							
							
Finalmente, los principales resultados fueron representados mediante un dashboard interactivo desarrollado en Google Sheets, que permite explorar los datos aplicando diferentes filtros

							
2. Descripción del dataset							
							
El dataset utilizado contiene información sobre diferentes características personales, educativas y laborales de una población adulta. La variable objetivo utilizada para el análisis es salary, que clasifica los registros en dos categorías de ingresos: <=50K y >50K. El resto de variables son las siguientes:							
										
	age:	Edad de la persona					
	workclass:	Tipo de clase laboral					
	education:	Nivel educativo					
	education-num:	Nivel educativo expresado numéricamente					
	marital-status:	Estado civil					
	occupation:	Ocupación					
	relationship:	Relación familiar					
	race:	Grupo racial					
	gender:	Género					
	capital-gain:	Ganancias de capital					
	capital-loss:	Pérdidas de capital					
	hours-per-week:	Horas trabajadas semanalmente					
	native-country:	País de origen					
	salary:	Categoría de ingresos					
	fnlwgt:	Peso estadístico asociado al registro					
							
							
3. Limpieza y transformación							
							
Antes de realizar el análisis se llevó a cabo un proceso de limpieza y transformación con el objetivo de mejorar la calidad y consistencia de los datos.							
								
	Registros iniciales:	48.842					
	Registros duplicados: eliminados	52					
	Registros finales:	48.790					
	Valores '?':	Sustituidos por 'Unknown'					
	Columna eliminada "fnlwgt":	1					
	Corrección de formatos:	5 columnas - formato numérico					
							
Además, se crearon las variables salary_numeric, age_group, has_capital_gain, has_capital_loss y hours_group para facilitar la segmentación y el análisis descriptivo. Las mismas son columnas adicionales añadidas y resaltadas en color en el data set limpio.							
							
La variable fnlwgt se elimina en el dataset limpio ya que no se utilizó en el análisis descriptivo principal debido a que representa un peso estadístico y su interpretación requiere un tratamiento específico.							
							
							
4. Análisis exploratorio de los datos							
							
Una vez finalizado el proceso de limpieza, se realizó un análisis exploratorio mediante tablas dinámicas y gráficos con el objetivo de identificar patrones y diferencias en la distribución de los ingresos según distintas características de la población.							
							
							
4.1 Distribución de ingresos							
							
¿Cómo se distribuyen los registros entre las dos categorías de ingresos?							
							
La variable salary divide a la población analizada en dos categorías: <=50K y >50K. La mayor parte de los registros pertenece a la primera categoría (76,06%), mientras que una proporción menor corresponde a personas con ingresos superiores a 50K (23,94%).							
							
							
4.2 Nivel educativo e ingresos							
							
¿Cómo varía la distribución de ingresos según el nivel educativo?							
							
Se analizó la distribución de las categorías de ingresos según el nivel educativo (education_num). Los resultados muestran diferencias en la composición educativa de ambos grupos.

En el grupo de ingresos ≤50K, los niveles educativos con mayor representación son Some college (34,09%) y High school graduate (29,83%). Por su parte, en el grupo de ingresos >50K destaca especialmente el nivel Bachelor's, que representa el 31,96% de este grupo, seguido de Some college (26,03%) y High school graduate (20,09%).

La principal diferencia observada se encuentra en la representación de las personas con estudios universitarios: la categoría Bachelor's supone un 31,96% del grupo >50K, frente al 10,92% del grupo ≤50K. También se observa una mayor presencia relativa de niveles educativos superiores dentro del grupo de ingresos >50K.						
							
							
4.3 Género e ingresos							
							
¿Existen diferencias en la composición por género entre los grupos de ingresos ≤50K y >50K?							
							
Se analizó la composición de los grupos de ingresos según el género. En el grupo de ingresos ≤50K, los hombres representan el 61,18% y las mujeres el 38,82%. En cambio, dentro del grupo >50K, la representación masculina asciende al 84,86%, mientras que la femenina representa el 15,14%.							
							
Por tanto, se observa una diferencia importante en la composición por género entre ambas categorías de ingresos. El grupo >50K presenta una proporción masculina considerablemente superior a la observada en el grupo ≤50K.							
							
Este resultado refleja una asociación entre las variables género e ingresos dentro del dataset. No obstante, estos porcentajes describen la composición de cada grupo de ingresos y no representan directamente la probabilidad o porcentaje de personas de cada género que supera los 50K.							
							
							
4.4 Ocupación e ingresos							
							
¿Qué diferencias se observan en la distribución de las ocupaciones según el nivel de ingresos?							
							
La distribución de las categorías de ingresos también presenta diferencias según la ocupación. En el grupo ≤50K, las ocupaciones con mayor representación son Adm-clerical (13,04%), Craft-repair (12,72%) y Other-service (12,71%).

En el grupo >50K, la distribución cambia y destacan especialmente las categorías Exec-managerial (24,88%) y Prof-specialty (23,82%), seguidas de Sales (12,63%) y Craft-repair (11,83%).

Destaca especialmente el incremento de la representación de las ocupaciones Exec-managerial y Prof-specialty dentro del grupo >50K. La primera pasa de representar un 8,56% del grupo ≤50K a un 24,88% del grupo >50K, mientras que Prof-specialty pasa del 9,12% al 23,82%.

Por el contrario, algunas ocupaciones presentan una representación menor dentro del grupo >50K, como Adm-clerical, Handlers-cleaners y Other-service.

En conjunto, los resultados muestran diferencias en la distribución de los grupos de ingresos según la ocupación, aunque estas diferencias deben interpretarse como asociaciones descriptivas y no como relaciones causales.					
							
							
4.5 Edad e ingresos							
							
¿Cómo se distribuyen los diferentes grupos de edad entre las personas con ingresos ≤50K y >50K?							
							
Se observa una distribución diferente según el nivel de ingresos. En el grupo ≤50K, las personas se encuentran distribuidas principalmente entre los grupos de 17-25, 26-35 y 36-45 años, que en conjunto representan aproximadamente el 74% del total. En cambio, en el grupo >50K existe una mayor concentración en los grupos de 36-45 y 46-55 años, que representan aproximadamente el 63% del total.							
							
Esto muestra una asociación entre la edad y el nivel de ingresos, observándose una mayor concentración del grupo >50K en edades medias y una mayor presencia de personas jóvenes en el grupo ≤50K.							
							
En conjunto, los datos sugieren que la pertenencia al grupo de ingresos >50K es más frecuente en edades medias que en los grupos de menor edad.							
							
							
4.6 Horas trabajadas e ingresos							
							
¿Existe una diferencia en las horas trabajadas semanalmente entre las personas con ingresos ≤50K y >50K?							
							
Se observa una diferencia en el promedio de horas trabajadas semanalmente según el nivel de ingresos. Las personas con ingresos ≤50K trabajan una media de 38,84 horas semanales, mientras que aquellas con ingresos >50K alcanzan un promedio de 45,45 horas semanales.

La diferencia entre ambos grupos es de aproximadamente 6,61 horas semanales, lo que supone una mayor cantidad media de horas trabajadas entre las personas pertenecientes al grupo de ingresos superiores a 50K.

En conjunto, los resultados muestran una asociación entre las horas trabajadas y la categoría de ingresos, ya que el grupo >50K presenta un promedio de horas semanales superior. Sin embargo, estos datos no permiten determinar que trabajar más horas sea la causa de obtener mayores ingresos.							
							
4.7. Estado civil e ingresos							
							
¿Cómo se distribuyen las categorías de estado civil entre los diferentes grupos de ingresos?							
							
Se analizó la distribución del estado civil dentro de las dos categorías de ingresos (≤50K y >50K). Los resultados muestran diferencias en la composición de ambos grupos.							
							
En el grupo de ingresos ≤50K, las categorías con mayor representación son Never-married, Married-civ-spouse y Divorced. En cambio, dentro del grupo >50K, destaca especialmente la categoría Married-civ-spouse, que presenta una representación considerablemente mayor que en el grupo de ingresos ≤50K.							
							
También se observa una menor representación de las categorías Never-married, Divorced y Separated dentro del grupo >50K en comparación con el grupo ≤50K.									
En conjunto, los resultados muestran diferencias en la distribución del estado civil según la categoría de ingresos. En particular, el grupo >50K presenta una mayor concentración de personas pertenecientes a la categoría Married-civ-spouse, mientras que el grupo ≤50K presenta una distribución más repartida entre diferentes estados civiles.							
							
4.8. Ganancias de capital e ingresos							
							
¿Qué relación se observa entre la presencia de ganancias de capital y el nivel de ingresos?							
							
Al analizar la relación entre la presencia de ganancias de capital (has_capital_gain) y la categoría de ingresos (salary), los resultados muestran que el 95,84% de las personas con ingresos ≤50K no presenta ganancias de capital, mientras que el 4,16% sí las presenta. En el grupo con ingresos >50K, el 78,67% no presenta ganancias de capital y el 21,33% sí.							"							
							
Por lo tanto, se observa una mayor presencia de ganancias de capital dentro del grupo de personas con ingresos superiores a 50K. Esta diferencia representa una asociación observada en los datos, pero no permite establecer una relación de causalidad entre ambas variables.	
							
							
5. Dashboard							
							
A partir de los resultados obtenidos durante el análisis exploratorio se desarrolló un dashboard interactivo en Google Sheets. El dashboard permite visualizar de forma resumida los principales indicadores obtenidos y explorar los resultados mediante diferentes filtros.							
							
Se incorporaron indicadores KPI relacionados con la población analizada, los ingresos, la edad y las horas trabajadas, junto con gráficos que permiten comparar las principales características de los grupos de ingresos.							
							
Los controles de filtrado permiten analizar los resultados según diferentes características de la población y facilitan la exploración interactiva del conjunto de datos.							
							
							
6. Conclusiones							
							
El análisis realizado permite identificar diferentes patrones en la distribución de los ingresos según las características demográficas, educativas y laborales de la población analizada.							
							
En primer lugar, se observa una mayor concentración de personas con ingresos ≤50K, mientras que el grupo >50K representa una proporción menor del conjunto de datos. Al analizar las características de ambos grupos, se encuentran diferencias relevantes en cuanto al nivel educativo, género, ocupación y edad.							
							
En relación con el nivel educativo, el grupo >50K presenta una mayor representación de niveles educativos superiores, destacando especialmente la categoría Bachelor's. En cuanto a la ocupación, las categorías Exec-managerial y Prof-specialty tienen una presencia considerablemente mayor dentro del grupo >50K.							
							
Respecto a la edad, el grupo ≤50K presenta una distribución más equilibrada entre los grupos de edad más jóvenes, mientras que el grupo >50K se encuentra más concentrado entre los 36 y 55 años. Esto muestra una asociación entre la edad y la categoría de ingresos dentro del conjunto de datos.							
							
También se observan diferencias en la distribución por género, con una mayor representación masculina dentro del grupo >50K. Asimismo, las personas pertenecientes a este grupo presentan un promedio de 45,45 horas trabajadas semanalmente, frente a las 38,84 horas del grupo ≤50K.							
Por último, la presencia de ganancias de capital es considerablemente mayor dentro del grupo >50K: el 21,33% de este grupo presenta ganancias de capital, frente al 4,16% del grupo ≤50K.							
							
							
En conjunto, el análisis muestra que las categorías de ingresos están asociadas a diferentes características demográficas, educativas y laborales. Sin embargo, los resultados obtenidos son de carácter descriptivo y permiten identificar patrones dentro del dataset, pero no establecer relaciones de causalidad entre las variables.							
