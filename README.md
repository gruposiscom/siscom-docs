# SISCOM Docs

Sitio de documentación para **SISCOM** (Soluciones Integrales en Sistemas Computacionales). Este proyecto contiene documentación técnica, tutoriales y guías de procesos relacionados con administración de sistemas y tecnologías de la información.

## Contenido

El sitio incluye:

- **Tutoriales de Linux**: Guías para instalar Ubuntu Server, configurar Oh My Zsh, usar FreeRDP y diagnosticar almacenamiento
- **Procesos**: Documentación de procedimientos como instalación de Windows
- **Documentación general**: Recursos adicionales sobre sistemas computacionales

## Tecnología

Este sitio está construido con [Docusaurus](https://docusaurus.io/), un generador moderno de sitios web estáticos.

## Sitio en Producción

El sitio está desplegado en GitHub Pages:

- URL: [https://gruposiscom.github.io/siscom-docs/](https://gruposiscom.github.io/siscom-docs/)

## Scripts disponibles

- docusaurus: ejecuta el CLI de Docusaurus; base para otros comandos.
- start: levanta el servidor de desarrollo con hot‑reload.
- build: genera el sitio estático en build/ (HTML/CSS/JS listos para publicar).
- predeploy:gh-pages: corre npm run build antes de deploy:gh-pages.
- deploy:gh-pages: publica la carpeta build/ a la rama gh-pages usando el paquete gh-
  pages.
- swizzle: copia/expone componentes internos de Docusaurus para personalizarlos.
- deploy: usa el deploy oficial de Docusaurus (publica a gh-pages).
- clear: limpia cachés y artefactos locales de Docusaurus.
- serve: sirve el build local (build/) para verificarlo antes de publicar.
- write-translations: genera archivos base para traducciones.
- write-heading-ids: genera ids de headings en markdown (útil para migraciones).

## Autor

Desarrollado por Armando Ruiz ([@ruizamdev](https://github.com/ruizamdev)) para Grupo Siscom
