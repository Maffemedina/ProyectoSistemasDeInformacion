# PROYECTO SISTEMAS DE INFORMACIÓN
## DESERSIÓN DE ESTUDIANTES EN PREGRADO Y POSGRADO DE LA UPTC EN EL AÑO 2020 Y 2021-1
### Introducción
La educación juega un papel fundamental en la búsqueda del desarrollo y el bienestar social, especialmente por su impacto, en dos aspectos primordiales y complementarios como condición para la equidad social, o como base para el mejoramiento de la competitividad y la productividad.
La Universidad Pedagógica y Tecnológica de Colombia (UPTC) es una universidad pública, financiada principalmente por el Estado Colombiano, acreditada en alta calidad multicampus, con sede principal en la ciudad de Tunja. Es la universidad más importante del departamento de Boyacá y una de las más prestigiosas en el Estado Colombiano por su nivel académico, haciendo presencia en 8 departamentos del país.
El presente estudio pretendió identificar las variables personales, académicas y socioculturales que incrementan la probabilidad de deserción de los estudiantes de pregrado en la Universidad Pedagogica y Tecnologica de Colombia , con el fin de proponer estrategias institucionales para la disminución del riesgo de desertar

### Tecnologias Usadas
###### SQL Server Management Studio
![](https://miro.medium.com/max/402/1*KTDZHTVaVbvbyhIf2PmBAw.png)
###### Jupyter Notebook (google Colab)
![](https://tigue.com/static/d61d46c29725f1c0d1a8bb6dfbaf9ca1/11d19/jupyter_book_to_colab.png)
###### Power BI
![](https://crol.mx/wp-content/uploads/2021/01/PowerBI-Logo.png)
### Contexto Del Problema
La deserción en el pregrado es uno de los problemas mas recurrentes que enfrenta la educación superior; en la actualidad, la deserción acumulada al semestre llega a niveles cercanos al 50% en Colombia. Este fenómeno ha sido objeto de estudio recurrente, entre otras razones, por los costos que puede generar para los Estados, la sociedad y las instituciones de educación superior (IES). Altas tasas de desempleo, bajos ingresos, dificultades para el desarrollo personal y profesional, entre otras, son consecuencias de la deserción; sus implicaciones sociales y económicas son suficientes para considerarla una problemática a ser enfrentada con políticas y acciones puntuales. 

### Preguntas de negocio o Estratégicas
#### Preguntas Cuantitativas
- - ¿CUAL SEDE TIENE LA MAYOR DECERSION DE ESTUDIANTES?
- -¿CUANTOS HOMBRES Y CUANTAS MUJERES DESERTARON EN LOS AÑOS COMPRENDIDOS?
- - TENIENDO EN CUENTA LA JORNADA, MODALIDAD Y PERIODO ¿Cuál FUE LA UNIDAD DE ESTUDIO CON MAS DESERTORES?
- - ¿CUAL ES LA UNIDAD DE ESTUDIO CON MAS DESERTORES EN TODA LA POBLACION?
- - ¿EN QUE PERIODO HUBO MENOS DESERCION ESTUDIANTIL?

#### Preguntas Cualitativas
- ¿QUE FACTORES PUEDEN INFLUIR EN LA DESERCION ESTUDIANTIL?
- -¿CUÁLES SERÍAN LAS ESTRATEGIAS INSTITUCIONALES QUE PODRÍAN REDUCIR LA PROBABILIDAD DE ABANDONO DE LOS ESTUDIANTES?
### Muestra de datos y análisis
Conjuto de datos tomado de [Datos Abiertos](http://https://www.datos.gov.co/dataset/DESERCION-ACADEMICA-PREGRADO-Y-POSGRADO/3iew-7wpx "Datos Abiertos")

![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/DESERCION_ACADEMICA_PREGRADO_Y_POSGRADO.csv)

![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/SEDESMASDESERRTADAS.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/GENERODESERTO.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/PROGRAMA-MOD-JORN%20MAS%20DES.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/PROGRAMA-GENERAL-DESERT.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/A%C3%91OMASDESERCION.png)

### Código de Jupyter Notebook
 -  SE IMPORTAN LAS LIBRERIAS QUE VAMOS A NECESITAR PARA EL ENTRENAMIENTO DEL MODELO
-  LOS ÁRBOLES DE DECISIÓN SON MODELOS PREDICTIVOS FORMADOS POR REGLAS BINARIAS (SI/NO) CON LAS QUE SE CONSIGUE REPARTIR LAS OBSERVACIONES EN FUNCIÓN DE SUS ATRIBUTOS Y PREDECIR ASÍ EL VALOR DE LA VARIABLE RESPUESTA.
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/1%20PERCEPTRON.png)
 -  SE CONVIERTE EL ARCHIVO CSV EN UN DATAFRAME DE PANDAS
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/2%20PERCEPTRON.png)
-  SE AGRUPAN LOS DATOS  POR NOMBRE DE PROGRAMA Y DICE CUAL ES EL PROGRAMA CON MAS DESERCIONES, Y SE ORDENA DE MANERA DESCENDENTE
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/3%20PERCEPTRON.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/4%20PERCEPTRON.png)
-  SE PASAN LOS VALORES COMO ENTEROS , POR QUE SE CAPTAN COMO STRING
-  SE TRASPONE LA COLUMNA DE VERTICAL A HORIZONTAL
-- COLUMNA (0)=NOMBRE_PROGRAMA
-- COLUMNA (1)=NUMERO DE ESTUDIANTES DESERTORES
- SE CREA O SE LLAMA EL MODELO DE INTELIGENCIA ARTIFICIAL (ARBOL DE DESICION) , DONDE SE ESCOGE CUALQUIER VALOR ALEATORIO DE INICIO Y LO GUARDA EN LA VARIABLE REGRESOR, Y COMO CUALQUIER MODELO SE TIENE QUE ENTRENAR PARA PREDECIR (COMO DIVIDE LOS DATOS)
-  SE LE PASA X,Y PARA ESTE MODELO NO TENGO QUE DEFINIRLE EL NUMERO DE ITERACIONES SINO QUE EL ITERA HASTA DONDE TIENE QUE ITERAR
-  A PARTIR DE 7 REPETICIONES CUAL SERIA EL PROGRAMA EN EL QUE MAS DESERTAN 
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/5%20PERCEPTRON.png)
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/6%20PERCEPTRON.png)

- EN ESTE DIAGRAMA DE DISPERSION PODEMOS VER QUE CON 7 APARICIONES APARECE EL PROGRAMA 2 , pero le quedaria mas difcil de decidir donde fueran  2, 3 , 4 ,6 apariciones.
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/PREDICCION.png)

![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/7%20PERCEPTRON.png)
-  ¿EN QUE SE BASA EL ARBOL PARA TOMAR UNA DESICION SI CORRESPONDE A UN PROGRAMA O A OTRO? EN EL NUMERO DE APARICIONES
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/9%20PERCEPTRON.png)
- EL ARBOL DE DESICION ES PEQUEÑO PORQUE TENIA POQUITOS PROGRAMAS Y MUY POCAS APARICIONES 
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/10%20PERCEPTRON.png)
### Graficas Power BI
![](https://github.com/Maffemedina/ProyectoSistemasDeInformacion/blob/main/GRAFICASPOWERBI.png)

### Conclusiones
1. El programa academico con mas desertores tendra que crear unas nuevas estrategias en sus unidades o en los docentes que sean mas llamativos y no permitan que el estudiante desista
2. En el ejemplo los estudiantes con mas tendencia a desertar son los hombres ¿Porque? se tendria que perfilar mas a fondo los estudiantes para saber  variables como el nivel de escolaridad de los padres, el estrato socioeconómico, riesgo de abandono, la edad de inicio de los estudios y el género, entre otras.
3.  Fue posible encontrar un modelo de predicción basico que nos muestra el programa academico que mas tiene estudiante desertores

# GRACIAS
## Maria Fernanda Medina Vega
####Estudiante Ingenieria de Sistemas
