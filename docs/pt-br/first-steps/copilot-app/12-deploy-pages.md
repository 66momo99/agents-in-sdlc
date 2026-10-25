---
title: "Lição 12 - Implante o site com o GitHub Pages"
description: "Use o app do GitHub Copilot para configurar um workflow do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o workflow e orientar a implantação, mas cabe a você revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a implantação no GitHub Pages.
- revisar o workflow e o pull request antes de fazer o merge.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma maneira simples de testá-lo. Publicar o site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do app do Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama em três etapas: pull request do space-quiz mesclado; execução bem-sucedida do GitHub Actions para implantar o site, com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede que o agente crie e mescle um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de implantação e as solicitações de aprovação do GitHub.

## Revise o workflow e verifique a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as alterações do pull request, incluindo as etapas de build e implantação do workflow.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação tenha sucesso e o site esteja carregando.

## Resumo e próximas etapas

Agora o Space Quiz está disponível como um site publicado, e você verificou a implantação em vez de confiar apenas no relato do agente. Continue para a [Lição 13: revisão e próximas etapas][next-lesson].

[next-lesson]: ../13-review/
