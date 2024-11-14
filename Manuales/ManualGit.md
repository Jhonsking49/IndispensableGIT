# Manual de Git

## Índice
- [Manual de Git](#manual-de-git)
  - [Índice](#índice)
  - [Introducción a Git y GitHub](#introducción-a-git-y-github)
  - [Configuración Inicial](#configuración-inicial)
  - [Comandos Básicos de Git](#comandos-básicos-de-git)
    - [1. Inicializar un Repositorio](#1-inicializar-un-repositorio)
    - [2. Clonar un Repositorio](#2-clonar-un-repositorio)
    - [3. Añadir cambios al Área de Staging](#3-añadir-cambios-al-área-de-staging)
    - [4. Confirmar cambios](#4-confirmar-cambios)
    - [5. Enviar cambios a GitHub](#5-enviar-cambios-a-github)
    - [6. Descargar cambios desde GitHub](#6-descargar-cambios-desde-github)
    - [7. Ver historial de cambios](#7-ver-historial-de-cambios)
  - [Trabajando con Ramas](#trabajando-con-ramas)
    - [1. Crear una nueva rama](#1-crear-una-nueva-rama)
    - [2. Cambiar a una rama](#2-cambiar-a-una-rama)
    - [3. Crear y cambiar a una rama](#3-crear-y-cambiar-a-una-rama)
    - [4. Eliminar una rama](#4-eliminar-una-rama)
    - [5. Listar ramas](#5-listar-ramas)
    - [6. Unir ramas](#6-unir-ramas)
  - [Sincronizacion con GitHub](#sincronizacion-con-github)
    - [1. Sincronizacion con GitHub](#1-sincronizacion-con-github)
    - [2. Subir cambios a repositorio remoto](#2-subir-cambios-a-repositorio-remoto)
    - [3. Descargar cambios desde repositorio remoto](#3-descargar-cambios-desde-repositorio-remoto)
    - [4. Listar repositorios remotos](#4-listar-repositorios-remotos)
  - [Solucion de Conflictos](#solucion-de-conflictos)
  - [Recursos Adicionales](#recursos-adicionales)

---

## Introducción a Git y GitHub

**Git** es un sistema de control de versiones distribuido que permite gestionar el historial de cambios de un proyecto, facilitando la colaboración y el desarrollo en equipo. **GitHub** es una plataforma basada en Git que permite almacenar y colaborar en proyectos de manera remota, proporcionando herramientas adicionales para revisar, integrar y publicar el código.

---

## Configuración Inicial

Es necesario configurar Git con tus datos personales antes de empezar a trabajar.

1. **Configurar nombre y correo:**
    ```bash
    git config --global user.name "Tu Nombre"
    git config --global user.email "tuemail@example.com"
    ```
    Configura el nombre y correo del usuario, para que queden registrados en cada commit.

2. **Verificar configuración actual:**
    ```bash
    git config --list
    ```
    Muestra la configuración actual de Git, incluyendo nombre, correo y otras preferencias.

3. **Configurar editor de texto predeterminado:**
    ```bash
    git config --global core.editor "code --wait" # Ejemplo para Visual Studio Code
    ```
    Establece el editor de texto predeterminado para Git, útil para escribir mensajes de commit o resolver conflictos.

---

## Comandos Básicos de Git

A continuación se muestran los comandos esenciales para trabajar con Git en cualquier proyecto.

### 1. Inicializar un Repositorio
   ```bash
   git init
   ```

### 2. Clonar un Repositorio
   ```bash
   git clone <Url del repositorio>
   ```

### 3. Añadir cambios al Área de Staging
   ```bash
   git add <archivo>
   git add .
   ```

### 4. Confirmar cambios
   ```bash
   git commit -am "Mensaje del commit"
   ```

### 5. Enviar cambios a GitHub
   ```bash
   git push origin master
   ```

### 6. Descargar cambios desde GitHub
   ```bash
   git pull origin master
   ```

### 7. Ver historial de cambios
   ```bash
   git log
   git log --oneline
   ```

## Trabajando con Ramas

Las ramas permiten trabajar en paralelo sobre distintas características o versiones de un proyecto, facilitando la colaboración y el desarrollo de nuevas ideas sin afectar la rama principal.

### 1. Crear una nueva rama
   ```bash
   git branch <nombre_rama>
   ```
   Crea una nueva rama con el nombre especificado.

### 2. Cambiar a una rama
   ```bash
   git checkout <nombre_rama>
   ```

### 3. Crear y cambiar a una rama
   ```bash
   git checkout -b <nombre_rama>
   ```

### 4. Eliminar una rama
   ```bash
   git branch -d <nombre_rama>
   ```

### 5. Listar ramas
   ```bash
   git branch
   ```

### 6. Unir ramas
   ```bash
   git checkout <nombre_rama_principal>
   git merge <nombre_rama>
   ```

## Sincronizacion con GitHub

Para colaborar y sincronizar cambios con un repositorio remoto en GitHub, es necesario realizar algunas configuraciones y comandos adicionales.

### 1. Sincronizacion con GitHub
   ```bash
   git remote add origin <url_del_repositorio>
   ```

### 2. Subir cambios a repositorio remoto
   ```bash
   git push -u origin master
   ```

### 3. Descargar cambios desde repositorio remoto
   ```bash
   git pull origin master
   ```

### 4. Listar repositorios remotos
   ```bash
   git remote -v
   ```

## Solucion de Conflictos

Los conflictos ocurren cuando dos personas o ramas modifican la misma línea de un archivo. Git marca estos conflictos para que el usuario pueda resolverlos.

1. Identificar el conflicto: Git marcará los archivos en conflicto en el área de staging.
2. Editar el archivo en conflicto para decidir que cambios quieres conservar.
3. Añadir el archivo modificado al área de staging:
   ```bash
   git add <archivo>
   ```
4. Hacer un commit de la solución:
   ```bash
   git commit -m "Mensaje del commit"
   ```


## Recursos Adicionales

- [Documentacion oficial de Git](https://git-scm.com/doc)
- [Documentacion de Github](https://docs.github.com/es)


