# AAS PCF-Challenge
**Create your DPP 4.0 with Submodels Digital Nameplate and Carbon Footprint**

### Architecture Guardrail
![PCF Architectural Guardrail](images/Architecture_Guardrail.png)

### Your local AAS test environment: Mnestix Browser with BaSyx AAS Environment
Download this repository and run in your command line ```docker compose -f 'Mnestix\docker-compose.yaml' up```\
Mnestix-API  publishes the Demo AAS on startup to the BaSyx AAS Environment.
You will get:
- Demo AAS (json): http://localhost:8081/shells/aHR0cHM6Ly9hYXMyLnVuaS1oLmRlL2Fhcy9sbmkwNzI5
- Demo Carbon Footprint Submodel (json): http://localhost:8081/submodels/aHR0cHM6Ly9hYXMyLnVuaS1oLmRlL3NtL2xuaTA3MjlfUENG
- Demo Digital Nameplate Submodel (json): http://localhost:8081/submodels/aHR0cHM6Ly9hYXMudW5pLWguZGUvc20vYUhSMGNITTZMeTloWVhNeUxuVnVhUzFvTG1SbEwyRmhjeTlzYm1rd056STVfRE5Q
- Demo AAS in the Mnestix Browser: http://localhost:3000/en/viewer/aHR0cHM6Ly9hYXMyLnVuaS1oLmRlL2Fhcy9sbmkwNzI5
- Mnestix API Swagger-UI: http://localhost:5064/swagger/index.html
- BaSyx Environment API Swagger-UI: http://localhost:8081/swagger-ui/index.html

### Needed Submodel Templates
- Digital Nameplate: https://github.com/admin-shell-io/submodel-templates/tree/main/published/Digital%20nameplate/3/0
- Carbon Footprint: https://github.com/admin-shell-io/submodel-templates/tree/main/published/Carbon%20Footprint/0/9

### AAS Creator
There are many possibilities to create AAS:
- Creating a single AAS: Eclipse Package Explorer: https://github.com/eclipse-aaspe/package-explorer
- Creating AAS simple by filling json-templates
    - Take the provided demo Submodels as a template a replace placeholders 
    - node-RED might be a good tool for starting: https://nodered.org/
- Creating AAS with DataIngest-Endpoint of Mnestix-API
    - http://localhost:5064/swagger/index.html#/AasCreator
    - http://localhost:5064/swagger/index.html#/DataIngest/DataIngest_AddDataToAas
    - Docs: https://hub.docker.com/r/mnestix/mnestix-api
- Creating AAS programmatically with SDK:
    - BaSyx Python SDK: https://github.com/eclipse-basyx/basyx-python-sdk 
- Validating created AAS:
    - https://twinfix.twinsphere.io/ 
    - https://github.com/admin-shell-io/aas-test-engines

### Grafana and Telegraf
See: https://grafana.com/grafana/dashboards/928-telegraf-system-dashboard/?pg=dashboards&plcmt=featured-dashboard-4

### Home of Mnestix
https://github.com/eclipse-mnestix

### Screenshots of demo AAS in Mnestix Browser
- Submodel Digital Nameplate
![Mnestix Browser Digital Nameplate](images/Mnestix-Browser_DigitalNameplate.png)
- Submodel Carbon Footprint
![Mnestix Browser Carbon Footprint](images/Mnestix-Browser_CarbonFootprint.png)