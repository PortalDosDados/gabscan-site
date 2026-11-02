# 🌐 GabScan • Website Oficial & Política de Privacidade

Repositório público do website institucional e da documentação legal de conformidade (LGPD) do **GabScan** — aplicativo móvel para correção óptica de gabaritos (OMR) 100% offline.

---

## 🔗 Links Oficiais de Acesso

* **Website Principal:** [https://gabscan.com.br](https://gabscan.com.br)
* **Política de Privacidade (LGPD):** [https://gabscan.com.br/politica-privacidade.html](https://gabscan.com.br/politica-privacidade.html)
* **Canal Alternativo GitHub Pages:** [https://portaldosdados.github.io/gabscan-site/](https://portaldosdados.github.io/gabscan-site/)

---

## 📱 Sobre o GabScan

O **GabScan** é o assistente definitivo para professores e escolas, projetado para transformar a câmera de qualquer smartphone Android em uma poderosa leitora óptica de provas com processamento **100% On-Device** (sem necessidade de internet e custo zero de infraestrutura na nuvem).

### Principais Recursos Apresentados no Site:
1. **Motor OMR On-Device em Dart:** Reconhecimento em menos de 0.5s por folha com homografia 3x3 e correção geométrica automática de perspectiva e rotação.
2. **Auditoria Visual Transparente:** Círculos verdes nos acertos, vermelhos com "X" nos erros e laranjas indicando a resposta oficial esperada.
3. **Economia Inteligente de Papel:** Emissão de gabaritos em PDF nos formatos 1 por folha (A4), 2 por folha (A5) ou 4 por folha (A6) com guias de corte ✂️, gerando até 75% de economia de papel.
4. **Quadro da Turma & Exportação CSV:** Histórico de notas, estatísticas de aprovação e exportação de relatórios para Microsoft Excel e Google Planilhas.
5. **Diagnóstico Pedagógico de Distratores:** Painel estatístico que aponta quais alternativas funcionaram como "pegadinhas" e o índice de dificuldade de cada questão.
6. **OCR On-Device & Lista de Chamada:** Reconhecimento óptico inteligente do nome manuscrito do aluno no cabeçalho.
7. **Privacidade Total (LGPD):** Nenhuma foto ou dado pedagógico trafega por servidores externos.

---

## 📁 Estrutura de Arquivos

```
├── assets/
│   ├── icone_512x512.png                 # Ícone oficial de alta definição
│   ├── banner_1024x500.png                # Feature graphic promocional da Google Play
│   ├── screenshot_1_corretor.png          # Mockup Play Store: Tela do Corretor
│   ├── screenshot_2_emissao_pdf.png       # Mockup Play Store: Emissão de PDF & Economia
│   ├── screenshot_3_quadro_turma.png      # Mockup Play Store: Quadro da Turma & CSV
│   └── screenshot_4_analise_pedagogica.png# Mockup Play Store: Diagnóstico & Distratores
├── CNAME                                  # Apontamento de domínio personalizado (gabscan.com.br)
├── index.html                             # Landing page moderna e responsiva
├── politica-privacidade.html              # Termos de Privacidade e Conformidade LGPD
├── politica_privacidade.html              # Rota alternativa de compatibilidade
└── README.md                              # Documentação deste repositório
```

---

## ⚙️ Configuração de DNS (Registro.br)

Para vincular o domínio customizado `gabscan.com.br` a este repositório do GitHub Pages:

| Tipo | Nome / Host | Valor / Destino | Finalidade |
| :---: | :---: | :---: | :--- |
| **A** | `@` (raiz) | `185.199.108.153` | IP do servidor Anycast GitHub Pages |
| **A** | `@` (raiz) | `185.199.109.153` | IP do servidor Anycast GitHub Pages |
| **A** | `@` (raiz) | `185.199.110.153` | IP do servidor Anycast GitHub Pages |
| **A** | `@` (raiz) | `185.199.111.153` | IP do servidor Anycast GitHub Pages |
| **CNAME** | `www` | `portaldosdados.github.io.` | Redirecionamento canônico com SSL |

---

## 🗺️ Roadmap & Pendências de Lançamento

Tarefas técnicas vinculadas ao ciclo de publicação oficial do aplicativo:

- [ ] **Tornar o repositório de releases público**: Alterar a visibilidade de `PortalDosDados/gab_scan_releases` para público no lançamento oficial.
- [ ] **Reverter exclusão no CI**: Remover a flag `--exclude "https://github.com/PortalDosDados/gab_scan_releases.*"` do arquivo [.github/workflows/ci.yml](.github/workflows/ci.yml) para que o Lychee passe a auditar ativamente o link oficial de download contra status `200 OK`.

---

## 📬 Contato

* **E-mail Institucional:** [contatoportaldosdados@gmail.com](mailto:contatoportaldosdados@gmail.com)
* **Desenvolvido por:** Portal dos Dados

&copy; 2026 GabScan. Todos os direitos reservados.
