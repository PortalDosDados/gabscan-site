# 00-overview.md • Visão Geral & Escopo

## Escopo do Repositório
* Website institucional e documentação de conformidade legal (LGPD/Google Play Store) do aplicativo móvel GabScan [README.md].
* Atende aos pré-requisitos de aprovação na Play Store: Política de Privacidade e URL de suporte [README.md].

## Stack Tecnológica & Versões
* Runtime: `NÃO IDENTIFICADO` (não requer Node.js, Python ou bundler) [inspeção da raiz].
* Linguagens: HTML5 semântico e CSS3 puro [index.html; politica-privacidade.html].
* Hospedagem: GitHub Pages via DNS Anycast com domínio customizado `gabscan.com.br` [README.md; CNAME].
* Dependências / Frameworks: `NÃO IDENTIFICADO` (zero dependências externas ou pacotes npm) [index.html].

## Ciclo de Vida & Comandos
* Instalação: `NÃO IDENTIFICADO` (não há etapa de `npm install` ou gerenciador de pacotes) [inspeção da raiz].
* Execução local: `SUGESTÃO (confirmar)`:
  * Python 3: `python -m http.server 8000`
  * Node.js/npx: `npx serve .`
  * VS Code: extensão *Live Server*
* Build: Deploy contínuo automático direto pelo GitHub Pages na branch `main` [README.md].
* Lint / Validação: `npx --yes htmlhint "**/*.html"` executado no CI [.github/workflows/ci.yml].
* Testes & Links: Validação de links via Lychee action no CI [.github/workflows/ci.yml].

## Restrições Gerais
* SEMPRE manter o repositório como site estático puro, leve e de alta disponibilidade.
* NUNCA introduzir frameworks pesados ou etapas complexas de build sem aprovação explícita.
* NUNCA comitar chaves, credenciais ou arquivos `.env*`.
