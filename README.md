# azure_deploy_test
Testing deployment to Azure Webapp from GitHub through Actions

# Links
- [YouTube Video to generate simple FastAPI](https://youtu.be/cbASjoZZGIw?si=mW_yStDYRc-hU4vZ)
- [How to run a FatsAPI app from Azure appservice](https://learn.microsoft.com/en-us/azure/developer/python/tutorial-containerize-simple-web-app-for-app-service?tabs=web-app-fastapi)
- [How to set up Azure App settings](https://learn.microsoft.com/en-us/azure/app-service/configure-common?tabs=portal)

# Run 
## Local - Using unicorn
1. Clone & set up python venv : python -m venv venv --upgrade-deps
1. Install requirements : pip install -r requirements.txt
1. Run : uvicorn main:app --reload

## Local - Using Docker & gunicorn
1. Follow set upo instructions in linnk "How to run a FatsAPI app from Azure appservice"
1. docker build --tag fastapi-demo .
1. docker run --detach --publish 3100:3100 fastapi-demo
1. Test with http://127.0.0.1:3100/

## Azure appservice
1. Create a B1 Azure Webapp