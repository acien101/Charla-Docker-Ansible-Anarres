---
title: 4a parte - Anarres
author: Fran Acién y M0wer
theme: solarized
revealOptions:
    transition: 'slide'
---

## Anarres

Juntando un batiburrillo de lo anterior sale [anarres-org/anarres: An ansible
playbook to set up a GNU/Linux server. Services in docker. Security by
default.](https://github.com/anarres-org/anarres).

----

## ¿Qué es Anarres?

Un playbook de Ansible para desplegar una serie de servicios autogestionados.

Construye todo un ecosistema para desplegar cosas. Todos los despliegues siguen
la misma metodología, todos los archivos de datos están por defecto en el mismo
directorio.

----

## ¿Qué no es Anarres?

Anarres no es una librería, no añade funcionalidad. Simplemente es una forma de
juntar una serie de herramientas ya existentes.

---

## Ventajas

* Es *limpio*. No hay que *instalar* Anarres. Lo despliegas y listo. Tampoco
   hace falta utilizarlo para mantener los servicios, pero se puede utilizar.
* Requiere poco mantenimiento. Los Dockers se actualizan *solos* y los
   certificados SSL también se renuevan automáticamente.
* Facilidad de *backup*. Todos los datos persistentes de los servicios y BBDD
   asociadas se guardan por defecto en el mismo directorio. Con eso y las
   variables del playbook ya podríamos desplegar de nuevo el servidor en otra
   instancia.
* Es fácilmente ampliable gracias a que todos los servicios siguen la misma
   metodología de despliegue.

---

## !Enséñame el código!

<https://github.com/anarres-org/anarres/blob/ae819f1ccfd41466b95b4ba50b3768be359d61d2/full.yml#L553>
