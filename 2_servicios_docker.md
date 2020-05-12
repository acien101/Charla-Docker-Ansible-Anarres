---
title: 2a parte - Levantar servicios con Docker
author: Fran Acién y M0wer
theme: solarized
revealOptions:
    transition: 'slide'
---

# Levantar servicios con Docker

----

## ¿Qué servicios puedo desplegar con Docker?

Miles de dockers en [Docker Hub](https://hub.docker.com/).

Algunos ejemplos interesantes: [Gitea](https://docs.gitea.io/), [Drone](https://drone.io/), [CodiMD](https://github.com/hackmdio/codimd), [OpenVPN](https://openvpn.net/), [Nextcloud](https://nextcloud.com/), etc.

No hace falta instalar nada. Esta todo contenido en un Docker :fire:.

----

## Diferentes formas de desplegar un servicio con Docker

1. Con `$ docker run` (vista en la transparencias anteriores)
2. Utilizando `$ docker compose`
3. Utilizando systemd

----

### Utilizando Docker Compose

Útil, pero no está pensado para mantener el servicio a largo plazo

[Ejemplo de docker-compose](./ejemplos/2_servicios_docker/docker-compose.yml)


```
$ cd ejemplos/2_servicios_docker
$ docker-compose up
```

----

### Utilizando systemd

1. Crearemos el o los servicios
2. Los desplegaremos con `$ systemd start docker.NOMBRE_DEL_SERVICIO`

----

#### Servicios Docker con systemd

[Ejemplo aquí](./ejemplos/2_servicios_docker/docker.docker_example.service)

----

#### Ventajas de administrar contenedores con Systemd

Systemd es el gestor de servicios por defecto de la mayoría de distribuciones
GNU/Linux. Ventajas de gestionar con Systemd servicios basados en Docker:

* Integración con otros servicios. Gestión de dependencias: quiere (Wants),
  después de (After)...
* Registros (logs) centralizados en el sistema.
* Configuraciones estandarizadas para todo tipo de servicios.
