# Análisis del sector de telecomunicaciones(Internet)

El objetivo de este análisis es proporcionar el panorama a nivel global sobre el acceso a internet ya que simulamos la entrada de una empresa que quiere entrar al mercado Nacional de Argentina por lo cuál debemos de proporcionar la información necesaria para que la empresa tome decisiones de entrar al mercado.

# Fuente de datos
Los datos con los cuales se hace el análisis son proporcionados por 
- [ENACOM](https://indicadores.enacom.gob.ar/datos-abiertos) 
- [población de argentina](https://populationtoday.com/ar-argentina/)
- [Proveedores de servicios de Internet](dhttps://www.argentina.gob.ar/sites/default/files/isp_por_provincias_2.pdf)


# Desarrollo 
Para este análisis realicé ETL´s para obtener los datos por hoja del archivo de excel llamado Intenet, asi como otros archivos los cuales son:

Una vez que obtuve los datos y verifique el tipo de dato, campos nulos y que no hubiera registros duplicados realicé un análisis exploratorio de los datos para entrar en contexto y poder hacer una conexión a la base de datos MySQL para subir los datos.

Ya una vez con la base de datos desarrollé un dashboard para representar un story telling al cuál llegué por medio del EDA.

# EDA
Hay 3 archivos de EDA que conforme fui avanzando el mi análisis fui explorando más opciones y parte de ese análisis lo muestro en imagenes con descripciones de lo que fui encontrando en los datos.

Inicié mi análisis exploratorio checando las variables númericas y variables categóricas

![variables númericas](imagenes/variables_numericas.png)

Continué con la variable Categórica

![variable categórica](imagenes/variables%20categoricas.png)

Busqué outlayers
![outlayers](imagenes/outlayers.png)

hice algunos hallazgos...
# Hallazgos
La tendencia por acceso tecnológico es Cable-modem y fibra Óptica 

![tendencia por tecnología](imagenes/tendencia_de_accesos_por_tecnologia.png)

Sin embargo cuando analice por provincia hay un caso que llama mi atención y es la provincia de San Luis en la que predomina la conexión por wireless y al parecer el gobierno provincial de San Luis ha invertido en infraestructura WiFi con el plan San Luis A1000, de acuerdo 
al siguiente: [artículo](https://agenciasanluis.com/2022/08/31/815248-san-luis-es-la-provincia-mas-digital-del-pais/)

![Caso San Luis](imagenes/hallazgo_san_Luis.png)

![porcentaje San Luis](imagenes/hallazgo_san_luis_porcentaje.png)

Por lo que San Luis aparece en segundo lugar a nivel de uso de tecnología wireless con un 12% de accesos

Conexiones por provincia anualizadas

![vision global](imagenes/conexiones_por%20años.png)

# Dashboard en Power BI




# Recomendaciones y conclusiones

- La velocidad a tomar en cuenta para proporcionar el servicio de Internet podria ser de más 30 Mbps para que la población se sienta atraída 

- El tipo de tecnología que ha venido a la alza es cableModem , fibra óptica 

- La tecnología wireless el gobierno de la provincia de San Luis es quien esta invirtiendo.

- La tecnología ASDL ha venido disminuyendo a lo largo del tiempo.

- En la parte Norte del país existen mayor número de conexiones que en la parte Sur.

- Los Ingresos han venido creciendo en los últimos 3 años con más del 40 % con respecto al año anterior.

- De acuerdo a los datos se puede entrar a proporcionar el servicio a las provincias con mayor población ya que aún se tiene un margen de casi el 50% de mercado en la penetración por hogares.








