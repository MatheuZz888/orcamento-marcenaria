# Project Brief — Gerador de Orçamento para Marcenaria

**Versão:** 1.0  
**Data:** 05/04/2026  
**Ferramentas:** Antigravity + Claude Code  
**Status:** Planejamento

---

## O que é esse projeto

Um sistema web que recebe a descrição de um móvel (texto livre ou lista de materiais) e gera automaticamente um orçamento com preços atualizados, buscados via scraping em fornecedores online.

---

## Objetivo de aprendizado

Aprender na prática:
- Estruturação profissional de projeto (git, documentação, CLAUDE.md)
- Uso de agentes com Antigravity (Manager Surface + missões)
- Claude Code para ajustes precisos no terminal
- Web scraping real
- Integração com Claude API para interpretar texto livre
- Entrega de resultado em interface web

---

## Escopo

### Dentro do escopo
- Input por descrição livre de móvel (ex: "guarda-roupa 3 portas MDF")
- Input por lista de materiais já definida
- Scraping de preços em fornecedores a definir (descoberta é parte do projeto)
- Cálculo de orçamento com materiais + preços
- Interface web simples para visualização do orçamento

### Fora do escopo (por enquanto)
- Login/autenticação
- Salvar histórico de orçamentos
- Envio por email ou PDF
- Multi-usuário

---

## Stack (referência inicial — pode evoluir)

| Camada | Tecnologia |
|---|---|
| Backend | Python |
| Scraping | Playwright ou BeautifulSoup (definir no checkpoint 3) |
| IA (parse de texto) | Claude API (claude-sonnet-4-6) |
| Frontend | HTML + CSS + JS simples (sem framework) |
| Controle de versão | Git + GitHub |

---

## Checkpoints

### ✅ CP-00 — Project Brief
Documento de projeto criado e entendido.  
**Entregável:** Este arquivo.

---

### 🔲 CP-01 — Setup do Projeto
Estrutura de pastas, git init, GitHub repo, CLAUDE.md com contexto do projeto.  
**Entregável:** Repositório criado e estrutura base commitada.  
**Ferramentas:** Claude Code no terminal

---

### 🔲 CP-02 — Descoberta de Fontes de Preço
Pesquisar e testar quais sites de fornecedores de MDF/madeira permitem scraping.  
Documentar: URL, estrutura HTML do preço, limitações.  
**Entregável:** `docs/fontes-scraping.md` com pelo menos 2 fontes validadas.  
**Ferramentas:** Antigravity (browser agent para explorar sites)

---

### 🔲 CP-03 — Módulo de Scraping
Scraper funcional que recebe nome de material e retorna preço atual.  
**Entregável:** `src/scraper.py` com testes manuais documentados.  
**Ferramentas:** Claude Code + Antigravity

---

### 🔲 CP-04 — Parser de Descrição com IA
Integração com Claude API: recebe texto livre ("guarda-roupa 3 portas") e retorna lista estruturada de materiais com quantidades.  
**Entregável:** `src/parser.py` com exemplos de input/output testados.  
**Ferramentas:** Claude Code

---

### 🔲 CP-05 — Motor de Orçamento
Combina parser + scraper: lista de materiais → preços → orçamento calculado.  
**Entregável:** `src/budget.py` rodando end-to-end no terminal.  
**Ferramentas:** Claude Code + Antigravity

---

### 🔲 CP-06 — Interface Web
Frontend simples: campo de input, botão gerar, tabela de orçamento.  
**Entregável:** App rodando em localhost, orçamento visível no navegador.  
**Ferramentas:** Antigravity (browser agent para validar UI)

---

### 🔲 CP-07 — Revisão Final
Código limpo, README completo, CLAUDE.md atualizado, último commit.  
**Entregável:** Repositório em estado "mostrável" para portfólio.

---

## Estrutura de Pastas (target)

```
marcenaria-orcamento/
├── CLAUDE.md           ← contexto para Claude Code
├── README.md           ← descrição do projeto
├── docs/
│   └── fontes-scraping.md
├── src/
│   ├── scraper.py
│   ├── parser.py
│   └── budget.py
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── tests/
└── requirements.txt
```

---

## Como usar este documento em um novo chat

Cole o seguinte no início da conversa:

> "Estou desenvolvendo o projeto Gerador de Orçamento para Marcenaria. Segue o Project Brief: [colar conteúdo deste arquivo]. Estamos no checkpoint [X]. Contexto atual: [descrever onde parou]."

---

## Notas e Decisões

| Data | Decisão | Motivo |
|---|---|---|
| 05/04/2026 | Fonte de scraping a definir no CP-02 | Precisamos validar quais sites permitem scraping antes de decidir a tecnologia |
| 05/04/2026 | Frontend sem framework | Reduzir complexidade — foco é aprender o fluxo, não React |
