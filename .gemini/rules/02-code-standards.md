# 02-code-standards.md • Padrões de Código & Estilização

## Padrões de HTML & Semântica
* SEMPRE declarar `<!DOCTYPE html>` e `<html lang="pt-BR">` [index.html: L1-2].
* SEMPRE incluir meta tags de responsividade (`viewport`), `description` e Open Graph (`og:*`) [index.html: L4-16].
* SEMPRE utilizar tags semânticas estruturais: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>` [index.html].
* SEMPRE definir atributos `alt` informativos em todas as tags `<img>` [index.html: L799].

## Padrões de CSS (OBSERVADO)
* Design System baseado em variáveis CSS no seletor `:root` (`--primary`, `--primary-light`, `--accent`, `--text-main`, `--bg-page`, `--border-color`) [index.html: L21-36].
* Reset básico universal aplicado: `* { box-sizing: border-box; margin: 0; padding: 0; }` [index.html: L38-42].
* Tipografia de sistema com fallback nativo (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto...`) [index.html: L45].
* Layouts responsivos implementados com CSS Grid e Flexbox via Media Queries `@media (max-width: ...)` [index.html: L516-600].
* PREFIRA manter estilos autocontidos em `<style>` para evitar falha de carregamento no crawler do Google Play Console.

## Convenções de Nomenclatura (OBSERVADO)
* Arquivos HTML: `kebab-case` (`politica-privacidade.html`), exceto o alias de compatibilidade `politica_privacidade.html` [README.md].
* Ativos de imagem: `snake_case` com dimensões ou descritor funcional (`banner_1024x500.png`, `icone_512x512.png`, `screenshot_1_corretor.png`) [assets/].
* Classes CSS: `kebab-case` descritivo (`.nav-wrapper`, `.section-header`, `.cta-banner`) [index.html].

## Anti-padrões Proibidos
* NUNCA utilizar bibliotecas pesadas de CSS/JS via CDN externo sem necessidade comprovada.
* NUNCA usar estilos inline (`style="..."`) onde classes CSS reutilizáveis forem aplicáveis.
* NUNCA introduzir links absolutos para recursos locais (ex.: `C:/...` ou caminhos locais do host).
