# Fontes de Scraping — Pesquisa CP-02

## Sites Viáveis

### 1. Gasômetro Madeiras (PRIORITÁRIO)
- URL: https://www.madeirasgasometro.com.br/
- Preços: visíveis sem login
- Estrutura: HTML estático, padrão VTEX
- URL produto: /[nome-do-produto]/p
- Bloqueio: baixo
- Tecnologia: BeautifulSoup (Python)

### 2. Madeiranit
- URL: https://www.madeiranit.com.br/
- Preços: visíveis sem login
- Estrutura: HTML estático
- URL produto: /[nome-do-produto]
- Bloqueio: baixo
- Tecnologia: BeautifulSoup (Python)

### 3. Mestre Marceneiro
- URL: https://www.mestremarceneiro.com/
- Preços: visíveis sem login
- Estrutura: HTML estático
- URL produto: /[linha-do-produto]/p
- Bloqueio: baixo
- Tecnologia: BeautifulSoup (Python)

## Sites Descartados
- Leo Madeiras: bloqueio + geolocalização obrigatória
- GMAD: preços carregam via JavaScript
- Rimad: firewall agressivo, inviável

## Decisão
Começar pelo Gasômetro Madeiras no CP-03.
Biblioteca escolhida: BeautifulSoup + requests (Python)