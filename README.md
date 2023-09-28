# jupyter BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

After the docker installation follow these [instructions](INSTALL-APP.md).

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-jupyter
cd app-jupyter
docker network create bibbox-default-network
docker-compose up -d
```

The main App can be opened and set up at:
```
http://localhost:8888
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the store. Click on the symbol and select install. Then fill the parameters below and name your App, click install again.

## Docker Images used
  - [jupyter/datascience-notebook](https://hub.docker.com/r/jupyter/datascience-notebook) 


 
## Install Environment Variables
  - JUPYTER_TOKEN = Configures Jupyter Notebook to require the given plain-text token. Should be combined with USE_HTTPS on untrusted networks. Note that this option is not recommended for production!

  
The default values for the standalone installation are:
  - JUPYTER_TOKEN = token

  
## Mounted Volumes
### jupyter/datascience-notebook Conatiner
  - *./notebooks:/home/jovyan/work*

