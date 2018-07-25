# Devops-vagrant-ansible-docker
Desafio devops mezclando vagrant, ansible y docker, para poder hacer manejo mas agil de la infraestructura:

El desafio tiene 2 grandes partes:

1) Crear una maquina virtual con Vagrant y provisionar un docker engine con Ansible.
 
2) Desplegar una aplicación dockerizada sobre la VM usando Ansible y docker-compose.

Solucion:

Para dar respuesta a la primera parte:
- Instalaré virtualbox en mi notebook, para tener un ambiente de virtualizacion.
- Tambien instalaré vagrant en mi notebook, para poder hacer manejo como codigo del aprovisionamiento en virtualbox.
- Aprovisionaré con vagrant en virtualbox, levantaré una maquina virtual ubuntu 16.04.
- Durante el aprovisionamiento con vagrant, con comandos de shell instalaré ansible en la maquina virtual ubuntu 16.04.
- Durante el aprovisionamiento con vagrant, con comandos de ansible-playbook local instalaré docker engine.

Para dar respuesta a la segunda parte:
- Ya teniendo la maquina operativa (ubuntu 16.04) con ansible instalaré docker compose
- Teniendo todos los archivos de configuracion, con ansible gatillaré la ejecucion de docker compose.
- Al gatillar la ejecucion de docker compose desplegaré una aplicacion web con phython a partir de una imagen docker.

La estructura de los archivos para reproducir el escenario esta en la imagen:


- Crear un repositorio en Github con todos los archivos necesarios para crear la infraestructura virtual y un README file con la documentación para replicar el escenario y un diagrama que explique el flujo.
 
