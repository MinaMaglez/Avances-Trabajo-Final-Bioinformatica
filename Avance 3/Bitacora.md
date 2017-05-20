# Bitacora de avances del trabajo final

### Carmina Martinez Gonzalez

##### *06/abril/2017*

#### Problemas con la computadora que tenia partición Windows/Biolinux, se murio la tarjeta madre (osea se murio la computadora)

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

#### *03/mayo/2017*

#### Cambio de sistema operativo de Windows a Ubuntu 10.6 en computadora hp con procesador intel Atom

#### *04/mayo/2017*

#### Se intento instalar Docker pero no se logro, ya que la computadora es de 32 bits

#### Se busco la forma de instalar el programa STACKS en la computadora y encontre el contenedor "Bioconda", se instalo Bioconda en la computadora pero no se logro instalr STAKCS a partir de este contenedor debido a que el progrmaa solo estaba disponible para computadoras de 64 bits

#### *05/mayo/2017* al *08/mayo/2017*

#### Se intento instalar Docker en Windows-HOME de una computadora de 64 bits y a partir de ahi instalar STACKS en un contenedor, por alguna razon los contendores se creaban pero al salir ya no me dejaba volver a entrar y decia que el contenedor no existia

#### *09/mayo/2017*

#### Se particiono la computadora de 64bits en Windows/Biolinux, la particion tomo todo el dia por alguna razon

#### *10/mayo/2017* al *15/mayo/2017*

#### Se intento instalar Docker y Bioconda en Biolinux, no se logro 
#### Busque tutoriales en youtube para instalar Docker y por alguna razon mis videos corrian demasiado rapido y no se escuchaban, trate de solucionarlo y no lo consegui

#### *16/mayo/2017*

#### Consegui la computadora de mi hermana y se particiono en Windows/Ubuntu 16.04, aprendi la valiosa leccion de que las computadoras hp no se llevna bien con biolinux 

#### Instale Docker, y cree la imagen del contenedor Anaconda

#### *17/mayo/2017*

#### Monte un volumen en el que me permitiera tener mis archivos y mediante la imagen de Anaconda instale Stacks

#### Intente correr los analisis y descubri que el formato de mis datos (genepop) no me permitiria correr mis analisis en Stacks, ya que estos requieren un formato VCF

#### *18/mayo/2017*
#### Una compañera de clase me comento que mis datos se podian anilizar con paqueterias de R, asi que en decidi cambiar de progama y analizar los datos con distintas paqueterias de R en lugar de usar Stacks

#### Instale las librerias necesarias y comenze a hacer pruebas para correr mis analisis, pero mi base de datos no cargaba correctamente

#### *19/mayo/2017*

#### Encontre que el problema con mi base de datos era que en los nombres de los loci incluian "|", y R leia eso como un comando, asi que reemplace todos los "|" por "_" y la base de datos se cargo correctamente

#### Realice los estadisticos basicos, pero aun tengo que averiguar como hacer el analisis de componentes principales



