# Gramática e tokens

## Tokens reconhecidos

| Texto | Token | Exemplo |
| --- | --- | --- |
| Uma sequência de dígitos | `NUM` | `42` |
| `+` | `PLUS` | `2 + 3` |
| `-` | `MINUS` | `7 - 1` |
| `*` | `TIMES` | `2 * 4` |
| `/` | `DIVIDE` | `8 / 2` |
| `(` e `)` | `LPAREN`, `RPAREN` | `(2 + 3)` |

Espaços, tabulações e quebras de linha são ignorados pelo lexer.

## Regra atual

A produção central em `parser/parser.y` é equivalente a:

```text
expressao : expressao operador expressao
          | '(' expressao ')'
          | NUM
```

O `operador` pode ser `+`, `-`, `*` ou `/`. A aceitação sintática não calcula o resultado: as ações semânticas ainda serão adicionadas em uma próxima etapa.

## Próximos incrementos

- Definir precedência e associatividade dos operadores.
- Adicionar ações para avaliar expressões ou construir uma AST.
- Melhorar mensagens com posição da entrada.
- Criar casos de teste para entradas válidas e inválidas.