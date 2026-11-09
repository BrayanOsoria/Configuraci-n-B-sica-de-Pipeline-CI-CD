# Práctica 3 - Pipeline CI/CD con GitHub Actions

Este repositorio contiene una aplicación web en Node.js/Express con un pipeline de Integración y Despliegue Continuo (CI/CD) configurado mediante GitHub Actions.

## Estructura del Pipeline
El flujo automatizado (`ci.yml`) consta de dos trabajos principales:
1. **Build & Test**: Se activa con cada `push` o `pull request` a la rama `main`. Configura el entorno Node.js, instala las dependencias (`npm ci`) y ejecuta las pruebas unitarias configuradas con Jest.
2. **Deploy**: Si el trabajo anterior es exitoso y el evento es un `push` a `main`, este paso despliega automáticamente el contenido estático de la carpeta `/public` a GitHub Pages.

## Instrucciones de Despliegue Local
Para ejecutar este proyecto en tu entorno local:
1. Clona el repositorio: `git clone <URL_DEL_REPO>`
2. Instala las dependencias: `npm install`
3. Ejecuta las pruebas: `npm test`
4. Inicia el servidor: `npm start` (El servidor correrá por defecto en el puerto configurado).

## Guía de Contribución
1. Haz un Fork del repositorio.
2. Crea una rama para tu nueva característica (`git checkout -b feature/NuevaCaracteristica`).
3. Haz commit de tus cambios (`git commit -m 'Añadir nueva característica'`).
4. Haz push a la rama (`git push origin feature/NuevaCaracteristica`).
5. Abre un Pull Request. El pipeline ejecutará automáticamente las pruebas para validar tu código.