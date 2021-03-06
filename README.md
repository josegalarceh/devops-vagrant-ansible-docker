# Devops-vagrant-ansible-docker
Desafio devops mezclando vagrant, ansible y docker, para poder hacer manejo mas agil de la infraestructura:

El desafio tiene 2 grandes partes:

1) Crear una maquina virtual con Vagrant y provisionar un docker engine con Ansible.
 
2) Desplegar una aplicación dockerizada sobre la VM usando Ansible y docker-compose.

Solucion:

Para dar respuesta a la primera parte:
1) Instalaré virtualbox en mi notebook, para tener un ambiente de virtualizacion.
2) Tambien instalaré vagrant en mi notebook, para poder hacer manejo como codigo del aprovisionamiento en virtualbox.
3) Aprovisionaré con vagrant en virtualbox, levantaré una maquina virtual ubuntu 16.04.
4) Durante el aprovisionamiento con vagrant, con comandos de shell instalaré ansible en la maquina virtual ubuntu 16.04.
5) Durante el aprovisionamiento con vagrant, con comandos de ansible-playbook local instalaré docker engine.

Para dar respuesta a la segunda parte:

6) Ya teniendo la maquina operativa (ubuntu 16.04) con ansible instalaré docker compose.
7) Teniendo todos los archivos de configuracion, con ansible gatillaré la ejecucion de docker compose.
8) Al gatillar la ejecucion de docker compose desplegaré una aplicacion web con phython a partir de una imagen docker.

La estructura de los archivos para reproducir el escenario estan en la imagen "Estructura archivos.png", pero basicamente se ordena de la siguiente forma
- Carpeta vagrant: Carpeta principal donde van alojados todos los archivos.
- Carpeta sharedfiles: Carpera compartida, donde se alojan los archivos necesarios para correr ansible y docker en la maquina virtual. Esta carpeta se comparte al momento de crear la maquina virtual con vagrant y permite disponibilizar los codigos dentro de la maquina de forma rapida.
- Carpeta compose: Carpeta donde estan todos los archivos necesarios para desplegar aplicacion con docker compose.

Se deben descargar todos los archivos segun la estructura anterior descrita. 

Para poder ver la aplicacion, al final deberiamos poder meternos a un explorador dentro del notebook a la url: 192.168.100.101:5000
Similar a lo de la imagen: "Resultado aplicacion.png"
 
