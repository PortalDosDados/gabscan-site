# 01-architecture.md • Arquitetura & Estrutura de Diretórios

## Padrão Arquitetural
* Arquitetura *Vanilla Web* de arquivos estáticos planos servidos na raiz [README.md].
* Autocontenção: páginas HTML com estilos CSS embutidos em tags `<style>` para garantia de renderização sem dependências externas [index.html; politica-privacidade.html].

## Mapa de Diretórios e Responsabilidades
* `/`: Raiz do website [README.md: L30-45].
  * `index.html`: Landing page institucional do app GabScan [index.html].
  * `politica-privacidade.html`: Política de Privacidade e Conformidade LGPD exigida pelo Google Play Console [politica-privacidade.html].
  * `politica_privacidade.html`: Cópia idêntica de compatibilidade de rota com underscore [README.md: L43].
  * `CNAME`: Configuração de domínio customizado (`gabscan.com.br`) [CNAME].
  * `README.md`: Documentação técnica, tabela DNS e links oficiais [README.md].
* `assets/`: Ativos visuais estáticos (PNG/MP4) [README.md: L32-41].
  * `icone_web.png`: Ícone otimizado para web (navbar e favicon) [assets/].
  * `icone_512x512.png`: Ícone oficial em alta resolução [assets/].
  * `banner_1024x500.png`: Feature graphic promocional da Play Store [assets/].
  * `screenshot_*.png`: Capturas de tela e mockups da aplicação [assets/].
  * `tutorial_gabscan.mp4`: Vídeo tutorial oficial na Hero Section [assets/].

## Regras de Acoplamento & Importação
* SEMPRE utilizar caminhos relativos para ativos internos (ex.: `assets/icone_web.png`) [index.html].
* SEMPRE manter `politica-privacidade.html` e `politica_privacidade.html` 100% idênticos [README.md].
* NUNCA remover ou alterar o conteúdo do arquivo `CNAME` (`gabscan.com.br`) [CNAME].
* NUNCA alterar o link de inscrição do Beta Fechado ou URLs oficiais sem validação prévia [index.html].
