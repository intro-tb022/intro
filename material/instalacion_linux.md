Material: Cómo instalar Linux
========

Existen varias formas de instalar un sistema operativo Basado en Linux:

- Instalación Nativa: creando una partición en un disco duro que ya tenga instalado otro sistema operativo o en otro disco vacío.

- Virtualización: cuando el sistema operativo corre sobre otro sistema operativo en forma de programa

    - Máquina Virtual: el SO guest corre en un ambiente controlado por el SO host. Todos los recursos son virtuales y otorgados por el SO host, por lo que requieren de muchos recursos y son más lentos.
    - Windows Sussytem for Linux: una aplicación de Windows dedicada exclusivamente a soportar un sistema Linux de manera virtual. Los recursos son compartidos con el SO host de manera directa sin perder performance.

# Instalación Nativa

[Guía oficial para instalar Ubuntu de manera nativa ](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview)

Cubre tanto la instalación como único SO y junto con otro como partición.

La guía está enfocada en la distribución de Ubuntu, pero cualquier otra distribución se puede usar en su lugar reemplazando el archivo .iso

[Lista de distribuciones que usan GNOME](https://www.gnome.org/getting-gnome/)

# Virtualización

## Máquina Virtual

Se debe primero instalar en el sistema operativo host (asumimos que Windows) un programa para manejar máquinas virtuales. El más usado es [VirtualBox](https://www.virtualbox.org/), [QEMU](https://www.qemu.org/) es una alternativa un poco más avanzada.

Una vez instalado el programa, se debe conseguir el archivo .iso con la imagen de la distribución que deseemos.

Seguir la guia de instalación de cada una para realizar la instalación.
- [Guia VirtualBox](https://www.virtualbox.org/manual/UserManual.html#create-vm-wizard)

## WSL

Hoy en día la herramienta es muy poderosa y cumple todas las necesidades que podamos llegar a tener. Se uso es muy sencillo. Es recomendado y avalado oficialmente por Canonical (empresa que mantiene la distribución de Ubuntu).

Pueden seguir los [tutoriales recomendados por ellos mismos](https://ubuntu.com/desktop/wsl)

De usar este tipo de instalación, pueden también utilizar [esta extensión de VSCode](https://code.visualstudio.com/docs/remote/wsl) que permite conectarse a la distribución desde Windows mismo.