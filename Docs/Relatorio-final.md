# Relatório Final – Dupla Samuel Guimarães Miranda e Samuel de Mendonça.

## ## O que aprendemos

* A diferença prática entre `display: block`, `inline` e `inline-block` ficou muito clara. `inline-block` é uma ferramenta poderosa para componentes de UI como botões e badges.
* Entendemos como o Box Model (margin/border/padding) se comporta de forma diferente em elementos de bloco e de linha.
* O processo de depuração forçada (criar bugs de propósito) é um excelente exercício para solidificar o conhecimento.
* Trabalhar de forma assíncrona com um colega, revisando o trabalho um do outro, melhora a qualidade do código e ajuda a identificar erros mais rápido.

## ## Diferenças entre LLMs

### LLM #1 (GPT-3.5-Turbo)
* **Pontos Fortes:** Rápido para gerar a estrutura base, código funcional e correto.
* **Pontos a Melhorar:** O código era um pouco mais verboso e os comentários, embora úteis, eram mais genéricos.

### LLM #2 (Gemini Pro)
* **Pontos Fortes:** Excelente capacidade de análise e depuração (encontrou todos os 4 bugs). O código gerado foi mais moderno e as explicações mais aprofundadas.
* **Pontos a Melhorar:** Em alguns momentos, a resposta pode ser mais longa por tentar fornecer mais contexto.

## ## Erros comuns e correções

1.  **Erro:** Tentar aplicar `width` ou `height` a um elemento `display: inline`.
    * **Antes:** `<span style="width: 100px;">Texto</span>` (Não funciona)
    * **Correção:** Mudar o display para `inline-block` ou `block`. `<span style="display: inline-block; width: 100px;">Texto</span>`

2.  **Erro:** Usar `margin-top` ou `margin-bottom` em um elemento `display: inline`.
    * **Antes:** `<span style="margin-top: 20px;">Texto</span>` (Não funciona)
    * **Correção:** Novamente, a solução é usar `display: inline-block` ou `block`.

3.  **Erro:** Confundir seletor de classe (`.`) com seletor de ID (`#`).
    * **Antes:** CSS: `#meu-item { ... }` / HTML: `<div class="meu-item">`
    * **Correção:** Garantir que o seletor no CSS corresponda ao atributo no HTML. CSS: `.meu-item { ... }`