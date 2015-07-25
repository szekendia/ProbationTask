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
* GeoTimeSeries.csv : annual data with geographic hierarchy (Country, Region, Sub-region, county). Data normalized from:
	* _Regisztralt_bunelkovetok.xls_
	* _Gazdasagilag_aktiv_nepesseg_szama.xls_
	* _Kozszolgaltatas_kereteben_elszallitott_telepulesi_hulladek.xls_
* TimeSeries.csv : time series of
* ops (sub-folder)
	* DataSource.csv : specifies the KSH files to be downloaded and normalized
* schema (sub-folder)
	* Schema_XML_generator.xlsx : Excel tool to generate schema XML content
	* SCHEMA_...xml : Supporting schema XML-s for faster metadata management