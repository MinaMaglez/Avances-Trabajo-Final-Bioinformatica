# Bitadora de avances del trabajo final


##### *14/abril/2017*

#### Revision de si se debia hacer de novo el alineamiento de las secuencias. 

#### - En la compilación de datos encontramos el archivo con los Cotings ya alineados, asi que no es necesario hacer un alineamiento de novo. 

##### *17/abril/2017*

#### Lectura del manual de STACKS para saber como hacer los analisis de estadisticos basicos de genetica de poblaciones
#### - Con la aplicacion "populations" dentro del programa STACKS podemos obtener los datos de Heterocigosis esperada y observada, π, Fis, Fst, y diversidad haplotipica. 

##### *21/abril/2017*

#### Lectura detallada del metodo utilizado en el articulo Funk et al., 2016 para obtener los parametros con los que realizan los analisis estadisticos de genetica de poblaciones basica. 

#### Los autores no calculan parametros de genetica poblacional basica, por lo que no puedo basarme en ningun parametro de ellos. 

#### Se buscara algun otro articulo en el que si hagan los analisis deseados.

##### *24/abril/2017*

#### Revision de que necesito para realizar los analisis 

#### - Para poder utilizar la aplicación de STACKS "populations" se debe creae un mapa de poblaciones, que es un archivo de texto con solo dos columnas, la primera columna se pone la identidad de cada muestra, mientras que en la seguna columna se indica la poblacion (Es preferible indicar la población con letras y no con numeros). 

#### *Ejemplo:* 

```
% more popmap 
indv_01<tab>SMI
indv_02		SMI 
indv_03		SMI 
indv_04		SCA 
indv_05		SCA 
indv_06		SCA 
```

#### Para calcular los valores de π, Fis, Fst  y diversidad haplotipica se usara el siguiente codigo 

```
~/% populations -P ./stacks/ -M ./samples/popmap -b 1 -k -t 36
```

###### No entiendo que es y para que es -b (batch_id)

###### Aun no me queda claro en que momento cargas la base de datos con los SNP's y en que formato deben ir estos. 

#### Para el analisis de Fst con la obtencion del p-value se usara el siguiente codigo

```
~/% populations -P ./stacks/ -M ./samples/popmap -b 1 -k -f p_value -t 36
```

