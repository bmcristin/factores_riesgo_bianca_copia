# Proyecto de Data Science: Análisis de Factores de Riesgo en la Salud

## Introduccion
Este proyecto es parte del trabajo final para el curso de Data Science dictado por Fundación YPF - 2024

Este proyecto tiene como objetivo identificar y evaluar los factores de salud que pueden influir en el desarrollo de diversas enfermedades en las personas. Factores como la diabetes, el tabaquismo, la hipertensión y otros parámetros de salud serán analizados para determinar su impacto en la aparición de enfermedades.

La identificación temprana y precisa de estos factores de riesgo es crucial para desarrollar estrategias de prevención y tratamiento más efectivas. A través de técnicas de análisis de datos y modelos predictivos, buscamos aportar una visión integral y basada en datos que pueda ayudar a mejorar la salud pública y la calidad de vida de las personas.

Este README proporciona una visión general del proyecto, incluyendo los objetivos, la metodología utilizada, las herramientas y los resultados esperados. Esperamos que esta documentación sea útil tanto para los profesionales de la salud como para los científicos de datos y cualquier persona interesada en la intersección entre la ciencia de datos y la salud pública.

## Objetivo
Desarrollar un modelo predictivo para identificar individuos con alto riesgo de
desarrollar enfermedades crónicas (como hipertensión, diabetes, colesterol alto) basándose
en sus comportamientos y condiciones de vida.

## Integrantes GRUPO 7
* Romina Torres
* Camila Breide
* Bianca Cristin

## Datasets utilizados
Utilizaremos las bases de datos proporcionadas por el Indec para el año 2018
https://www.indec.gob.ar/indec/web/Institucional-Indec-BasesDeDatos-2
En la seccion salud, especificamente : "Encuesta Nacional de Factores de Riesgo (ENFR)"
De ser necesario para el proyecto, ampliaremos el uso a las bases de datos correspondientes a los años 2005, 2009 y 2013

El diccionario de registros puede encontrarse en el siguiente link:
https://docs.google.com/spreadsheets/d/1Sb_nay9oorUlxbLbh2d-kRkgiVJ69FBDOMVkDEll8sw/edit?usp=sharing

La encuesta utilizada para la captura de datos puede encontrarse en el siguiente link:
https://www.indec.gob.ar/ftp/cuadros/sociedad/cuestionario_enfr_2018.pdf

## Estructura del repositorio
* README.md
* acondicionamiento.ipynb - archivo donde se realiza el renombre de columnas y limpieza general de los bloques temáticos
* analisis_exploratorio.ipynb
* datasets - carpeta con los archivos correspondientes a todos los años
*    | friesgo2018.txt
* utils - carpeta con archivos de utilidad
*    | codificaciones.py - diccionarios correspondientes a toda la codificacion usada en los datasets
*    | funciones.py - funciones creadas para el uso comun en todo el analisis 

## Organizacion del trabajo

### Bloques temáticos
Para un procesamiento eficiente y organizado, agruparemos las columnas por bloques tematicos. Para mas detalles de las columnas en cada bloque, remitirse al final de este README.

* Ubicacion
* Características del encuestado
* Salud general
* Actividad física
* Tabaquismo 
* Hipertensión 
* Peso corporal 
* Alimentación 
* Colesterol 
* Consumo alcohol 
* Diabetes
* Mediciones antropometricas
* Mediciones bioquimicas

### Limpieza de datos
Este archivo contiene los pasos necesarios para la limpieza del dataset
* Agrupamiento de las columnas en los bloques temáticos antes mencionados
* Renombre de columnas por nombres más explícitos
* Creación y cálculo de nuevas columnas
* Identificación del tipo de variables utilizadas en cada bloque temático

### Análisis exploratorio
Este archivo contiene los pasos necesarios para realizar el análisis exploratorio de los datos, en una primera instancia, se tratan los bloques temáticos identificados en el archivo limpieza_datos.csv. Luego, todos los bloques temáticos se unifican en un único DataFrame para continuar con el análisis exploratorio del dataset limpio en su conjunto.

El analisis exploratorio consiste en identificar y procesar estos puntos:
* Nulos
* Datos faltantes
* Outliers
* Colinealidad

Finalmente, se detectan 'Preguntas disparadoras' referidas al dataset final, que se responden mediante gráficos y analisis.

## Estructura del dataset
A continuacion se detalla cada bloque temático y sus respectivas variables

### Ubicacion
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |

### Características del encuestado
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |

### Salud general
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |

### Actividad física
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |

### Tabaquismo 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| bita01      | ¿Alguna vez fumó cigarrillos?      | var categorica      |
| bita02      | ¿Qué edad tenía cuando fumó por primera vez?       | var numerica       |
| bita02_99      | Ns/Nc (edad que tenía cuando fumó por primera vez)      | var numerica discreta      |
| bita03      | En toda su vida ¿ha fumado por lo menos 100 cigarrillos?      | var categorica      |
| bita04      | Actualmente ¿fuma usted cigarrillos…      | var categorica      |
| bita04_01      | Actualmente, ¿fuma cigarrillo armado?      | var categorica      |
| bita04_02      | Actualmente, ¿fuma cigarrillo de paquete?      | var categorica      |
| bita05      | ¿Qué marca de cigarrillos fuma habitualmente?      | var categorica      |
| bita06_a      | ¿Qué tipo de paquete compra habitualmente?      | var categorica      |
| bita06_b      | ¿De qué cantidad?       | var numerica discreta      |
| bita06_b_99      | ¿De qué cantidad? Ns/Nc      | var numerica discreta      |
| bita06_c      | ¿De qué sabor?      | var categorica      |
| bita06_d      | ¿Con qué tipo de cápsula?      | var categorica      |
| bita07      | Pensando en la última vez que compró cigarrillos de esta marca y variedad para su propio consumo, ¿cuánto dinero pagó por esa compra?      | var numerica continua      |
| bita07_99      | ¿cuánto dinero pagó por esa compra? - Ns/Nc      | var categorica      |
| bita08      | ¿Intentó dejar de fumar en el último año?      | var categorica      |
| bita09_01      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… cigarros o habanos?      | var categorica      |
| bita09_02      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… cigarritos?      | var categorica      |
| bita09_03      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… pipa común?      | var categorica      |
| bita09_04      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… pipa de agua?      | var categorica      |
| bita09_05      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… tabaco para masticar?      | var categorica      |
| bita09_06      | Actualmente, de los siguientes productos de tabaco que no son cigarrillos de paquete ni armados a mano, ¿usted consume… cigarrillo electrónico?      | var categorica      |
| bita10_01      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de su casa?      | var categorica      |
| bita10_02      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de su trabajo?      | var categorica      |
| bita10_03      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de instituciones educativas?      | var categorica      |
| bita10_04      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de bares/restaurantes?      | var categorica      |
| bita10_05      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de hospitales/centros de salud?      | var categorica      |
| bita10_06      | Durante los últimos 30 días, ¿notó que alguien fumó en alguno de los  siguientes lugares cerrados… dentro de otros lugares?      | var categorica      |
| bita11      | En los últimos 30 días, ¿Vio alguna publicidad de cigarrillos en comercios donde se venden cigarrillos?      | var categorica      |
| bita12      | En los últimos 30 días ¿recibio por correo electrónico publicidad de cigarrillos o material de promoción de cigarrillos?       | var categorica      |
| bita13      | En los últimos 30 días ¿se suscribio en alguna página web de una empresa que produce cigarrillos, una página web de una marca de cigarrillos o una página web que tuviera los logos de marcas de cigarrillos?       | var categorica      |
| bita14      | En los últimos 30 días, ¿vio alguna frase o imagen sobre el riesgo de fumar impresa en paquetes de cigarrillos?      | var categorica      |
| bita15      | ¿Las frases o imágenes que vienen en los paquetes de cigarrillos lo hicieron pensar en dejar de fumar?      | var categorica      |
| bita16      | ¿Está de acuerdo con el aumento del impuesto al tabaco?      | var categorica      |
| consumo_tabaco_100      | Condición de fumador      | var categorica      |
| ta_paquete_y_armado      | Prevalencia de consumo combinado de cigarrillos de paquete y armados      | var categorica      |
| ta_dejar_fumar      | Intentó dejar de fumar en el último año      | var categorica      |
| ta_otros_productos      | Consumo de al menos un producto de tabaco que no sean cigarrilllos      | var categorica      |
| hta_nofumadores      | Exposición de no fumadores al humo de tabaco ajeno en lugares cerrados      | var categorica      |
| ta_perc_publicidad      | Vio alguna publicidad de cigarrillos en comercios donde venden cigarrillos      | var categorica      |
| ta_percepcion_riesgo      | Vio alguna frase o imagen sobre el riesgo de fumar impresa en paquetes de cigarrillos      | var categorica      |
| imagenes_tabaco      | Pensó en dejar de fumar por las frases o imágenes de los paquetes de cigarrillos en los últimos 30 días      | var categorica      |

### Hipertensión 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |
### Peso corporal 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |
### Alimentación 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |
### Colesterol 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |
### Consumo alcohol 
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| Celda1      | Celda2      | Celda3      |
| Celda4      | Celda5      | Celda6      |
### Diabetes
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| bidi01      | ¿Alguna vez un médico, un enfermero u otro profesional de la salud le dijo que tenía diabetes o azúcar alta en la sangre?      | var categorica      |
| bidi02      | ¿Eso ocurrió cuando estaba embarazada?      | var categorica      |
| bidi03      | ¿En las últimas dos semanas, estuvo haciendo algún tratamiento (medicamentos, dieta, ejercicio) indicado por un profesional de la salud para mantener controlada su diabetes/azúcar en sangre?      | var categorica      |
| bidi04_01      | ¿Usted está haciendo algún tratamiento… con insulina?      | var categorica      |
| bidi04_02      | ¿Usted está haciendo algún tratamiento… con dieta,ejercicios, reducción de peso?      | var categorica      |
| bidi04_03      | ¿Usted está haciendo algún tratamiento… con medicamentos?      | var categorica      |
| bidi05      | ¿Es insulinodependiente?      | var categorica      |
| bidi06_01      | ¿Ha habido al menos un diagnóstico de diabetes entre sus familiares cosanguíneos directos (padres, hijos, hermanos)?      | var categorica      |
| bidi06_02      | ¿Ha habido al menos un diagnostico de diabetes entre otros familiares cosanguíneos (abuelos, tíos, primos)?      | var categorica      |
| bidi07      | ¿Cuando fue la última vez que le midieron glucemia/azúcar en sangre?      | var categorica      |
| bidi08      | ¿Excluyendo la medición de glucemia o azúcar en sangre, hay algún lugar al que usted vaya habitualmente para hacerse un control relacionado con la diabetes?      | var categorica      |
| bidi09      | Excluyendo la medición glucemia  y azúcar en sangre, ¿a qué lugar va habitualmente a hacerse esos controles?      | var categorica      |
| bidi10      | Cuando usted va a ese lugar, ¿siempre lo atiende el mismo profesional de la salud?      | var categorica      |
| bidi11      | ¿El médico o profesional que lo atiende en ese lugar conoce su historia clínica?      | var categorica      |
| bidi12      | En los últimos 12 meses, ¿un profesional de la salud le examinó los pies para detectarle heridas o irritaciones?      | var categorica      |
| bidi13      | En los últimos 12 meses, ¿le hicieron un examen de a vista en el que le dilataron las pupilas? (Este examen le habría ocasionado una sensibilidad temporal de luz brillante)      | var categorica      |
| bidi14      | ¿Ha tomado alguna vez un curso o una clase sobre cómo controlar usted mismo su diabetes?      | var categorica      |
| control_diabetes      | Medición de la glucemia/azúcar en sangre alguna vez por autorreporte      | var categorica      |

### Mediciones antropometricas
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| bima01      | ¿El encuestado firmó el consentimiento?      | var categorica      |
| bima02      | Esta mañana, ¿ha tomado café, café con leche, té, mate u otras bebidas que puedan contener cafeína?      | var categorica      |
| bima03      | ¿El encuestado consintió medirse la presión?      | var categorica      |
| bima04_01_a      | Primera medición/sistólica      | var numerica continua      |
| bima04_01_b      | Primera medición/diastólica      | var numerica continua      |
| bima04_02_a      | Segunda medición/sistólica      | var numerica continua      |
| bima04_02_b      | Segunda medición/diastólica      | var numerica continua      |
| bima04_03_a      | Tercera medición/sistólica      | var numerica continua      |
| bima04_03_b      | Tercera medición/diastólica      | var numerica continua      |
| promedio_sistolica      | Promedio de las dos últimas mediciones de tensión sistólica      | var numerica continua      |
| promedio_diastolica      | Promedio de las dos últimas mediciones de tensión diastólica      | var numerica continua      |
| ta_elevada      | Presión arterial elevada según mediciones físicas      | var categorica      |
| prevalencia_hipertension_combinada      | Prevalencia de presión arterial elevada por autorreporte y/o medición física      | var categorica      |
| bima06      | ¿El encuestado consintió medirse la altura?      | var categorica      |
| bima07      | Medición de la altura en centímetros      | var numerica continua      |
| bima09      | ¿El encuestado consintió pesarse?      | var categorica      |
| bima10      | Medición del peso en kilogramos      | var numerica continua      |
| imc_bima      | Índice de masa corporal según mediciones antropométricas      | var numerica continua      |
| imc_categorias_bima      | IMC agrupado según mediciones antropométricas      | var categorica      |
| bima12      | ¿El encuestado consintió medirse el perímetro de la cintura?      | var categorica      |
| bima13      | Perímetro de cintura en centímetros      | var numerica continua      |
| bima14      | Medición realizada      | var categorica      |

### Mediciones bioquimicas
| Variable | Descripción | Tipo de variable |
|-------------|-------------|-------------|
| bimq01      | ¿El encuestado firmó el consentimiento?      | var categorica      |
| bimq05      | Registre los valores de glucosa que le informe el personal de Salud [Medición en mg/dl]      | var numerica continua      |
| bimq05_01      | Valor no registrado por el dispositivo      | var categorica      |
| glucemia_elevada      | Glucemia elevada en mediciones bioquímicas      | var categorica      |
| prevalencia_glucemia_elevada_combinada      | Prevalencia de glucemia por autorreporte o medición bioquímica      | var categorica      |
| findrisc      | Riesgo de desarrollar diabetes mellitus en los próximos 10 años según puntaje FINDRISC      | var categorica      |
| bimq06      | Registre los valores de colesterol que le informe el personal de Salud [Medición en mg/dl]      | var numerica continua      |
| bimq06_01      | Valor no registrado por el dispositivo      | var categorica      |
| colesterol_elevado      | Colesterol elevado en mediciones bioquímicas      | var categorica      |
| prevalencia_colesterol_combinada      | Prevalencia de colesterol por autorreporte o medición bioquímica      | var categorica      |
