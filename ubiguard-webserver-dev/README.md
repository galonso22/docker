#ubiguard-webserver-dev

##Clonar proyecto
```sh
cd /home/galonso/dvlp/
git clone https://github.com/galonso22/docker.git
```
##Buildiar ubiguard-webserver-dev

```sh
cd /home/galonso/dvlp/docker/ubiguard-webserver-dev
make
```
###Para levantar el container

Configurar fig.yml con las rutas de los volumenes correctos.

```sh
figu up ubiguard-webserver-dev
```

Aparte hay que agregar en /etc/hosts:

172.17.0.23 iwaycam.localhost

La ip 172.17.0.23 seria la del container, para saber la ip de tu container ejecutar:

```sh
docker inspect IDCONTENEDOR
```
Esto ultimo hay que automatizarlo.