---
title: "Lección 12 - Despliega el sitio con GitHub Pages"
description: "Usa la aplicación de GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz en GitHub Pages para que cualquiera pueda acceder a ella. Copilot puede preparar el flujo de trabajo y guiarte durante el despliegue, pero eres responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pedirás a Copilot que configure el despliegue en GitHub Pages.
- revisarás el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- seguirás el despliegue y comprobarás el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero todavía hace falta una forma sencilla de probarla. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni dependencias de entorno de ejecución.

## Pide a Copilot que despliegue el sitio

En la sesión de la aplicación de Copilot para `space-quiz`, envía este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres etapas: una solicitud de incorporación de cambios de space-quiz combinada; una ejecución correcta de GitHub Actions para desplegar el sitio, con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz publicada en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de despliegue y las solicitudes de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba el despliegue

1. Confirma que el README solo se añade si el repositorio todavía no tiene uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Combina la solicitud solo cuando se hayan superado las comprobaciones requeridas.
4. Sigue la ejecución de despliegue de GitHub Actions hasta que termine correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede habilitar Pages o combinar la solicitud de incorporación de cambios, sigue las instrucciones concretas que te dé. No des la tarea por terminada hasta que el despliegue se complete y el sitio se cargue.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio y has comprobado el despliegue en lugar de confiar únicamente en el informe del agente. Continúa con [Lección 13: repaso y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
