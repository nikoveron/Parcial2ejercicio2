Paso 1: Construir las Imágenes Docker

Asegúrate de tener Docker instalado en tu sistema.

cd .\Rest\
docker build -t rest .

cd .\Soap\
docker build -t soap .

cd .\client\
docker build -t client .

cd .\mysql\
docker build -t db .

Paso 2: Desplegar en Docker Swarm
Inicializamos el Swarm:
docker swarm init

despliegue con Docker Stack:
docker stack deploy -c docker-compose.yml parcial2ejercicio2

Paso 3: Acceder al Cliente Web
Después de desplegar el stack, puedes acceder al cliente web desde tu navegador:

http://127.0.0.1:5500/client/index.html

Paso 4: Eliminar el Stack
Cuando hayas terminado, puedes detener y eliminar el stack con el siguiente comando:
docker stack rm parcial2ejercicio2
