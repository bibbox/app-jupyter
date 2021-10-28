
# Jupyter Notebook BIBBOX application

This container can be installed as [BIBBOX APP](http://bibbox.readthedocs.io/en/latest/admin-documentation/ "BIBBOX App Store") or standalone. 

* initial token for login has to be set during installation 

## Standalone Installation 

To install the app locally execute the commands:

`sudo git clone https://github.com/bibbox/app-jupyter`

`cd app-jupyter`

`docker network create bibbox-default-network`

`docker-compose up -d`

After the Installation open type

`docker logs local-jupyter`

At the bottom of the log file displayed there will be a link (starting with http://127.0.0.1:8888/?token=) you can follow to access the Notebook the token there will be set automatically

The default port of the app JupyterNotebook is 8888.

If necessary change the ports in the environment file .env and the volume mounts in `docker-compose.yml`.

## Install within BIBBOX

Follow the link above and find the App by its name. Click on the Symbol and select Install. Then fill the Parameters below and Name your app Click install again

## Docker Images used
 * [jupyter/datascience-notebook](https://hub.docker.com/r/jupyter/datascience-notebook/) 
 
## Install Environment Variables
  *	JUPYTER_TOKEN

The default values for the standalone installation are:
  * JUPYTER_TOKEN=token

## Mounted Volumes

### Jupyter Container
* _./notebooks_ will be mounted to _/home/jovyan/work_ (put your Notebooks into notebooks to have them in the container)
