README

Analisis de los datos obtenidos por Funk et. al., 2016 para 6 poblaciones de zorras isleñas (Urocyon littoralis) y una de zorras grises (Urocyon cinereoargenteus)

ID de las poblaciones 
	- grays = zorras grises del sur de California (continente) 
	- smi = zorras isleñas de la Isla San Miguel 
	- sri = zorras isleñas de la Isla Santa Rosa 
	- sci = zorras isleñas de la Isla Santa Cruz
	- sca = zorras isleñas de la Isla Santa Catalina
	- scl = zorras isleñas de la Isla San Clemente
	- sni = zorras isleñas de la Isla San Nicolas


Directorio de Urocyon_sp: 

	Data: 
		Poblaciones.csv --------> Relacion de nombre de la muestra con su localidad
		fox_GP1.gen ------------> Base de datos de los SNPs en formato genepop

	Imagenes:
		fox_ACP.jpg ------------> Imagen del analisis de componentes principales para todas las poblaciones

	R_scripts:
		Estadisticos_basicos.R -> Script para poder optener Ho y He por poblacion, y los estadisticos F por poblacion y globales
		ACP.R ------------------> Script para hacer el analisis de componentes principales y obtener una grafica de este
