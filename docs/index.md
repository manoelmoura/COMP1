# COMP1

## Compiladores 1, com as mãos no código

Um espaço de estudo para transformar expressões em tokens, tokens em árvores e ideias em um compilador compreensível.

!!! info "Ponto de partida"
    O projeto atual reconhece expressões aritméticas com números, operadores e parênteses. O objetivo é evoluir essa base por etapas, sempre deixando cada fase observável.

## Rota rápida

1. Instale as ferramentas descritas em [Como compilar](como-compilar.md).
2. Gere o parser e o lexer.
3. Alimente o executável com uma expressão, como `12 + 3 * (4 - 1)`.
4. Consulte a [arquitetura](arquitetura.md) para localizar cada responsabilidade.

<div class="status-strip">
  <span class="status-dot"></span>
  <span><strong>Estado atual</strong> · análise léxica + análise sintática</span>
</div>