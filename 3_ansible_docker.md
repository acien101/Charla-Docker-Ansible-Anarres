---
title: 3a parte - Docker y Ansible
author: Fran Acién y M0wer
theme: solarized
revealOptions:
    transition: 'slide'
---

# Automatizar despliege de servicios con Docker y Ansible

----

## Por qué Ansible

* Tareas repetitivas de levantar y actualizar.
* Mantener todos los deployments documentados.

----

## generic_docker_systemd

[Rol de Ansible para desplegar Docker con Systemd](https://github.com/anarres-org/generic_docker_systemd)

Básicamente un herramienta que nos rellenará una plantilla de *systemd* con un comando docker. Pero tiene bastantes funcionalidades para desplegar fácilmente *la gran mayoría* de servicios docker.

En su [readme](https://github.com/anarres-org/generic_docker_systemd/blob/master/README.md) hay bastantes ejemplos de desplegar un docker con una base de datos creando una red de docker, volumenes, variables de entorno, etc.

----

## Cómo sería levantar un servicio con generic_docker_systemd y Ansible

[Aquí vemos un ejemplo](./ejemplos/3_ansible_docker/main.yml)

Desplegar un docker con systemd en una máquina sería con:

```
$ ansible-playbook main.yml
```

---

## Levantar servicios, pedir certificados, configurar nginx y mucho más

Con el poder de **Ansible** seremos capaces de configurar muchas cosas además de los contenedores docker.

Todo eso es [Anarres](https://github.com/anarres-org/anarres). Un playbook de Ansible que configura un ecosistema para desplegar/mantener servicios fácilmente, configurando certificados,
