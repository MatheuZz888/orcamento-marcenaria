# Projeto: Gerador de Orçamento para Marcenaria

## O que é
Sistema web que recebe descrição de móvel (texto livre ou lista de materiais)
e gera orçamento com preços atualizados via scraping.

## Stack
- Python (backend + scraping)
- Claude API: claude-sonnet-4-6 (parser de texto livre)
- HTML + CSS + JS (frontend, sem framework)
- Git + GitHub (controle de versão)

## Estrutura
- src/ → código Python (scraper.py, parser.py, budget.py)
- frontend/ → interface web (index.html, style.css, script.js)
- docs/ → documentação e decisões
- tests/ → testes

## Checkpoints
- CP-01: Setup ← estamos aqui
- CP-02: Descoberta de fontes de scraping
- CP-03: Módulo de scraping
- CP-04: Parser com IA
- CP-05: Motor de orçamento
- CP-06: Interface web
- CP-07: Revisão final

## Regras
- Sempre commitar ao final de cada checkpoint
- Nunca commitar chaves de API (.env está no .gitignore)
- Comentar o código em português