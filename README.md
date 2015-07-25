# ProbationTask
## Probation Task of Talend and TIBCO Spotfire

### Repository content
Folder name | Content
----------- | -------
PROBATIONTASK.rar | Archive of the prepared Talend Open Studio project
KSH folder | KSH statistics prepared for data analysis

### PROBATIONTASK.rar
Download and extract the compressed file into the TOS Data Integrator's workspace folder. After extraction, import the project.
The jobs contain a custom component: tUnpivotRow [Talend Exchange: tUnpivotRow by daztop](https://exchange.talend.com/#marketplaceproductoverview:gallery=marketplace%252F1&pi=marketplace%252F1%252Fproducts%252F322%252Fitems%252F444)

### KSH folder
The folder contains the following files:
* __GeoTimeSeries.csv__ : TOS DI output file: annual data with geographic hierarchy (Country, Region, Sub-region, county). Data normalized from:
	* _6.2.7.3 A regisztrált bűnelkövetők (2000–2014)_
	* _6.2.1.7 A gazdaságilag aktív népesség száma (2000–2014)_
	* _6.5.3 A közszolgáltatás keretében elszállított települési hulladék keletkezése (2006–)_
* __TimeSeries.csv__ : TOS DI output file: longer time series of various statistics. Data normalized from:
	* _1.1 Population and vital statistics (1949-2015)_
	* _2.1 Employment and earnings (1960-2014)_
	* _2.6 Culture (1960-2014)_
	* _3.1.1 Gross domestic product (GDP) (1960-2013)_
* __ops__ (sub-folder)
	* DataSource.csv : specifies the KSH files to be downloaded and normalized
	* KSH_HU_geo_hierarchy.xlsx : geographic hierarchy
* __schema__ (sub-folder)
	* _Schema_XML_generator.xlsx_ : Excel tool to generate schema XML content
	* _SCHEMA_...xml_ : Supporting schema XML-s for faster metadata management
	* _errorlog.csv_ : Log file of download and FileInput errors (generated on 1st error)

### Probation Task project
The objective of the project is to download, load, transform (normalize) and extract specific KSH statistics.
The folder pathes used during the process are specified in global context variables:
* _Global.DATA_FOLDER_ : KSH statistics are downloaded into this folder, loaded from this folder and normalized output files are also exported to this location
* _Global.OPS_FOLDER_ : location of supporting operational files as described above
* _Global.SCHEMA_FOLDER_ : location of supporting SCHEMA files as described above
### Usage instructions
Open the KSH_LTE job and process it by pressing F6