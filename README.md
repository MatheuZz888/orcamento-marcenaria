# Gerador de Orçamento para Marcenaria

Sistema web que gera orçamentos automaticamente a partir da descrição
de um móvel, buscando preços atualizados via scraping.

## Como funciona
1. Usuário descreve o móvel (ex: "guarda-roupa 3 portas MDF") ou informa a lista de materiais
2. IA interpreta a descrição e extrai a lista de materiais com quantidades
3. Sistema busca preços atualizados nos fornecedores via scraping
4. Orçamento é exibido em interface web

## Stack
- Python
- Claude API (claude-sonnet-4-6)
- HTML + CSS + JS

## Status
🚧 Em desenvolvimento — CP-01 Setup