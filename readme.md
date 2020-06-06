# Curso de NPM Platzi

## Definición
NPM significa `Node Package Manager`

## Inicialización de npm
Existen opciones para la inicialización del proyecto, el principal es:
```bash
npm init
```
Este método nos preguntará por cada campo en el package.json, si se quiere una opción más rápida para ser llenada luego, se usa:
```bash
npm init -y
```
Esto nos creará un archivo limpio para completar.

## Agregar valores por defecto
En ocasiones queremos que ciertos valores sean los mismo, en ese caso utilizamos:
```bash
npm set init.author.name "Pedro Muñoz"
npm set init.author.email "pmunozb@protonmail.com"
npm set init.license "MIT"
```

En caso de querer eliminar una variable se usa:
```bash
npm config delete init.license
```
# Instalación de dependencias
## Producción
```bash
npm install moment --save
npm i moment -S
npm i moment
```
## Desarrollo
```bash
npm install moment --save-dev
npm i moment -D
```
## Global
```bash
npm i -g nodemon
```
Listar paquetes globales
```bash
npm list -g --depth 0
```
## Opcional
```bash
npm i eslint -O
```