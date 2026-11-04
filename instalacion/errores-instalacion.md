# ERRORES DE INSTALACIÓN

## 1. Comprobaciones Previas

**Revisar Requisitos** 
Comprobamos primero si el motor de Docker dispusiera de los recursos hardware mencionados 
- **4 GB de RAM libres**
- **CPU compatible con virtualización**
- **Espacio en disco**

## 2. Resolución de un problema típico

Una de las causas frecuentes de que el Docker no abra en Windows es que la virtualización esta desactivado.

Docker necesita virtualizacion por hardware por lo que tenemos que entrar a la BIOS y activarla .

Para poder comprobarlo en Windows tenemos que abrir el Administrador de tareas, meternos en el rendimiento hay vamos al CPU y por ultimo tenemos que meternos en Virtualización en este tiene que poner **Habilitada**.
