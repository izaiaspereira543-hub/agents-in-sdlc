---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz con GitHub Pages para que cualquiera pueda acceder. Copilot puede preparar el flujo de trabajo y guiarte durante la publicación, pero debes revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- Pide a Copilot que configure la publicación con GitHub Pages.
- Revisa el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- Sigue el proceso de publicación y comprueba el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero todavía hace falta una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él mediante una URL pública, sin añadir un servidor ni una dependencia del entorno de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación GitHub Copilot para `space-quiz`, envía este mensaje:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres etapas: solicitud de incorporación de cambios de space-quiz combinada; ejecución correcta de GitHub Actions para Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz disponible en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de publicación y cualquier solicitud de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba la publicación

1. Confirma que el archivo README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación y publicación del flujo de trabajo.
3. Combina la solicitud solo cuando se superen las comprobaciones obligatorias.
4. Sigue la ejecución de publicación de GitHub Actions hasta que termine correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede activar Pages o combinar la solicitud de incorporación de cambios, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la publicación se complete y el sitio esté disponible.

## Resumen y próximos pasos

Space Quiz ya está disponible como sitio y has comprobado la publicación en lugar de confiar en el informe del agente. Continúa con la [Lección 13: repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
