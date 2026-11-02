# 03-testing-and-quality.md • Qualidade, Play Store & Checklist

## Pré-requisitos da Google Play Store (DIRETRIZ)
* Conformidade da URL de Política de Privacidade: a rota deve retornar HTTP 200 permanentemente [README.md].
* Cláusula de Exclusão de Dados: a política DEVE manter explícito que o app é 100% offline e que a exclusão dos dados é realizada pelo usuário limpando o cache/dados do app ou desinstalando-o [politica-privacidade.html: L165-177].
* Dados de Contato: e-mail oficial `contato@gabscan.com.br` e menção ao desenvolvedor `Portal dos Dados` devem permanecer visíveis no rodapé e na política [README.md; politica-privacidade.html].

## Validação e Testes
* Validação Automatizada (CI): Execução de HTMLHint para sintaxe e Lychee para validação de links [.github/workflows/ci.yml].
* Exclusão Temporária do Repositório de Releases: O link `PortalDosDados/gab_scan_releases` está excluído temporariamente no Lychee via `--exclude` enquanto o repositório for privado. Deve ser reativado assim que o repositório for público (ver [README.md]).
* Teste Manual: validação visual via servidor HTTP local em resoluções Desktop e Mobile antes de qualquer publicação [SUGESTÃO (confirmar)].
* Validação de Links: testar todos os links de ancoragem interna (`#diferenciais`, `#economia`, etc.) e rotas externas.

## Checklist Obrigatório da IA Pré-Conclusão
Antes de finalizar qualquer tarefa ou alteração no repositório, a IA DEVE verificar:
1. [ ] **Integridade do CNAME**: O arquivo `CNAME` existe na raiz contendo exclusivamente `gabscan.com.br`?
2. [ ] **Sincronização da Política**: Se `politica-privacidade.html` foi alterada, `politica_privacidade.html` foi atualizada de forma idêntica?
3. [ ] **Responsividade**: As novas seções mantêm compatibilidade móvel (breakpoints `@media`)?
4. [ ] **Assets**: Nenhuma imagem ou recurso local quebrado (caminhos relativos corretos para `/assets/`)?
5. [ ] **Segurança**: Nenhum dado sensível, segredo ou arquivo `.env*` adicionado ao repositório?
6. [ ] **Escopo**: Nenhuma dependência desnecessária ou arquivo fora do escopo foi introduzido?
