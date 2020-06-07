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
## Simular instalación
```bash
npm i react --dry-run
```
## Forzar instalación
```bash
npm i webpack -f
npm i webpack --force
```
## Instalar una versión específica
```bash
npm i json-server@0.15.0
```
# Actualización
## Listar actualizaciones del proyecto
```bash
npm outdate
npm outdate --dd
```
## Actualizar un package
```bash
npm i json-server@latest
```
## Actualizar todos los paquetes
```bash
npm update
```
# Desintalación
## Quitar de carpeta node_modules y package.json
```bash
npm uninstall json-server
```
## Quitar solo de carpeta node_modules
```bash
npm uninstall json-server --no-save
```
# Símbolos
## Versionamiento
```
3.9.2

major . minor . patch

Major: Cambios mayores que pueden romper la compatiblidad.
Minor: Cambios menores, se refieren a nuevas funcionalidades, generalmente la compatibilidad se mantiene.
Patch: Corrección de errores.
```
## ^ (Caret, Acento circunflejo)
El símbolo indica que este paquete puede ser actualizado en su version minor y patch.
```json
"dependencies": {
    "json-server": "^0.15.1"
}
```
## ~ (Tilde, virgulilla)
El símbolo indica que este paquete solo puede ser actualizado en su version patch.
```json
"dependencies": {
    "json-server": "~0.15.1"
}
```
## Versión exacta
En ocasiones, es requerido tener una versión exacta del paquete, en ese caso, no se utilizan símbolos:
```json
"dependencies": {
    "json-server": "0.15.1"
}
```
## Versión mayor o mayor e igual
Si se requiere mantener que el paquete sea mayor a una versión o mayor e igual se utiliza:
```json
"dependencies": {
    "json-server": ">0.15.1",
    "moment": ">=2.26.0"
}
```
## Versión menor o menor e igual
Si se requiere mantener que el paquete sea menor a una versión o menor e igual se utiliza:
```json
"dependencies": {
    "json-server": "<0.15.1",
    "moment": "<=2.26.0"
}
```
# Caché
## Verificar datos en caché
```bash
npm cache verify
```
## Eliminar caché
```bash
npm cache clean --force
```
# Seguridad
## Verificar
```bash
npm audit
```
## Corregir errores
```bash
npm audit fix
```