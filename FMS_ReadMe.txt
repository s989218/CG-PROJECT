We have created following repositories in GIT, under organization OG-CTO-Predix
	- FMS      -  For webservice(Java Code)
	- FMS_DB   -  For DB scripts and
	- FMS_UI   -  For UI Code

Each repository has a branch Prod_Ph2, which has code for Prod deployment

Step 1: DB creation
Please execute the DB scripts in following sequence also in each folder we have numbered the script sequence in filename itself:

Folders:
- fms_sequences
- fms_table_scripts
- fms_types
- fms_views
- fms_functions
- fms_insert scripts

Step 2: Java code
##Rick to modify following file:
- In FMS -- Prod_Ph2 -- FMS\src\main\resources\application-prod.yml
The prod db details will need to be entered in application-prod.yml	
spring:
  datasource:
    url: 
    username: 
    password: 

Step 3: UI 
For FMS_UI we are using following UAA details, as used in QA, please modify as needed for Prod in manifest.yml:
      UAA_SERVER_URL: https://a8a2ffc4-b04e-4ec1-bfed-7a51dd408725.predix-uaa.run.aws-usw02-pr.ice.predix.io
      SERVICE_URL: https://fms.run.aws-usw02-pr.ice.predix.io/
      REDIS: redis-3
      clientId: oilgas_GEOG_DTSFM_dev
      uaa_authorization_header: b2lsZ2FzX0dFT0dfRFRTRk1fZGV2OjFUY05LVHluQzJESDNSeUY=
	  