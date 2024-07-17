# Análisis del sector de telecomunicaciones(Internet)

El objetivo de este análisis es proporcionar el panorama a nivel global sobre el acceso a internet ya que simulamos la entrada de una empresa que quiere entrar al mercado Nacional de Argentina por lo cuál debemos de proporcionar la información necesaria para que la empresa tome decisiones de entrar al mercado.


## Contenido
1. [Fuente de datos](#fuente-de-datos)
2. [Estructura del proyecto](#estructura-del-proyecto)
3. [Instalación](#instalación)
4. [Desarrollo](#desarrollo)
5. [EDA](#eda)
6. [Hallazgos](#hallazgos)
7. [Dasboard](#dashboard-en-power-bi)
8. [Conclusiones](#conclusiones)
9. [Contacto](#contacto)


# Fuente de datos
Los datos con los cuales se hace el análisis son proporcionados por 
- [ENACOM](https://indicadores.enacom.gob.ar/datos-abiertos) 
- [población de argentina](https://populationtoday.com/ar-argentina/)
- [Proveedores de servicios de Internet](https://www.argentina.gob.ar/sites/default/files/isp_por_provincias_2.pdf)
 
# Estructura del proyecto
- `datasetCrudos/`: Contiene los conjuntos de datos utilizados para analizar.
- `src/`: Contiene el ETL que ocupé para cargar los datos a una base de datos mySQL.
- `Notebooks/`: Contiene 3 archivos donde realice diferentes análisis exploratorios.
- `requirements.txt`: Lista de dependencias necesarias para ejecutar el proyecto.
- `Dashboard/`: Contiene el archivo pbix del dashboard creado
- `imagenes/`:Contiene imagenes de graficas y resultados del EDA asi como imagenes del dashboard 

## Instalación

1. Clona este repositorio:
    ```bash
    git clone https://github.com/OscarMoralesMejia/telecomunicaciones.git
    cd telecomunicaciones
    ```

2. Crea un entorno virtual y actívalo:
    ```bash
    python -m venv env
    source env/bin/activate  # En Windows usa `env\Scripts\activate`
    ```

3. Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```

# Desarrollo 
Para este análisis realicé ETL´s para obtener los datos por hoja del archivo de excel llamado Intenet, asi como otros archivos los cuales son:

- mapa_conectividad.xlsx
- Portabilidad.xlsx
- isp_por_provincias_2.pdf

Una vez que obtuve los datos y verifique el tipo de dato, campos nulos y que no hubiera registros duplicados realicé un análisis exploratorio de los datos para entrar en contexto y poder hacer una conexión a la base de datos MySQL para subir los datos.

El archivo ETL.ipynb está en la carpeta src

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

La fuente de datos de power BI es una base de datos hecha en mySQL

![base de datos](imagenes/bd_mysql.png)

Mediante la herramienta de Power BI realicé un dashboard para Generar un history telling en el cual podemos ver que hay muchas empresas proveedoras del servicio de internet, inicialmente vemos que las empresas son: claro y movistar las que están en el archivo de portabilidad, y al ver los datos notamos que va disminuyendo los clientes asi que nos dimos a la tarea de buscar mayor información y encontramos en datos del gobierno argentino que son 436 empresas registradas como proveedores de servicios de internet ubicadas por provincia.

![Empresas](imagenes/1_empresas.png)

En 2014 la velocidad predominante era 1-6 Mbps con el 80% de conexiones y en 2023 la velocidad predominante es más de 30 Mbps con el 68%.

Las 3 provincias que más conexiones tienen son: Buenos Aires, Capital Federal y Córdoba

![Accesos por velocidad](imagenes/2_accesosporvelocidad.png)

En San Luis y Formosa wireless esta ganando terreno San Luis esta en segundo lugar y Formosa en el lugar 10 a nivel de tecnologia wireless

Podemos ver el top 10 de provincias de acuerdo a la tecnología que más han venido utilizando 

![Accesos por tecnología](imagenes/3_accesosportecnologia.png)

En 2023 los ingresos por accesos a internet han crecido un 64% conrespecto al año anterior, 2022 creció por arriba del 40% asi como 2021.

![Ingresos](imagenes/4_ingresos.png)

En la parte norte del País de Argentina se nota mayor conectividadindependientemente de la tecnología usada.
Buenos Aires tiene casi el 50% de la población de Argentina
Tierra del Fuego ocupa el último lugar en población con apenas el 0.34% de población distribuida en la provincia

![Conectividad](imagenes/5_conectividad.png)

y por último nos proponemos objetivos en un idicador de rendimiento de Aumentar en un 2% el acceso a Internet por cada 100 hogares y observamos que en todas las provincias se llega al objetivo.

Tenemos otro KPI que tiene el objetivo de aumentar el acceso a internet independientemente de la tecnologia y vemos que en las provincias estuvieron muy cerca de alcanzar el objetivo.

Propusimos un tercer KPI con el objetivo de aumentar en un 2% el acceso a internet con la velocidad del mas de 30 Mbps ya que observamos que es la velocidad que más esta creciendo.

![KPI´s](imagenes/6_KPI.png)

# Conclusiones


**Velocidad de Internet:** La velocidad mínima recomendada para proporcionar el servicio de Internet debería ser superior a 30 Mbps para atraer a la población.

**Tecnologías en aumento:** Las tecnologías de CableModem y fibra óptica han mostrado un crecimiento significativo en su adopción.

**Inversión en tecnología wireless:** El gobierno de la provincia de San Luis es quien está realizando inversiones en tecnología inalámbrica (wireless).

**Declive de ADSL:** La tecnología ADSL ha experimentado una disminución del 50% en su uso a lo largo del tiempo analizado.

**Distribución geográfica de conexiones:** La región norte del país cuenta con un mayor número de conexiones en comparación con la región sur.

**Consideraciones para inversiones en el sur:** Invertir en la región sur podría requerir una mayor inversión debido a la menor densidad de población.

**Crecimiento de ingresos:** Los ingresos han crecido más del 40% anualmente durante los últimos tres años.

**Oportunidades de mercado:** De acuerdo con los datos, es viable proporcionar servicios de Internet en las provincias con mayor población, ya que aún existe un margen de penetración de mercado cercano al 50%.


# Contacto

[Linkedin](linkedin.com/in/oscar-m-7907294b)






