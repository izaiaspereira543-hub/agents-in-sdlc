---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e confirmar que o Space Quiz está no ar."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz com o GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a publicação, mas você continua responsável por revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot que configure a publicação pelo GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de mesclá-lo.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma maneira simples de testá-lo. Publicar o site composto por um único arquivo com o GitHub Pages o disponibiliza em uma URL pública, sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo GitHub Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama em três etapas: pull request do space-quiz mesclado; execução bem-sucedida de Deploy website no GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz no ar em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede que o agente crie e mescle um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de publicação e quaisquer solicitações de aprovação do GitHub.

## Revise o fluxo de trabalho e confirme a publicação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de compilação e publicação do fluxo de trabalho.
3. Mescle somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até a conclusão bem-sucedida.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até que a publicação seja bem-sucedida e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site, e você confirmou a publicação em vez de confiar no relato do agente. Continue para a [Lição 13: revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
