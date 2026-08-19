# Estrutura de arquivos

```text
.
├── lexer/lexer.l          # regras léxicas
├── parser/parser.y        # regras sintáticas
├── src/main.c             # ponto de entrada em evolução
├── lex.yy.c               # saída gerada pelo Flex
├── parser.tab.c           # saída gerada pelo Bison
├── parser.tab.h           # tokens gerados pelo Bison
├── compilador             # executável local
├── docs/                  # fonte deste site
└── mkdocs.yml             # configuração do MkDocs
```

Os arquivos C gerados e o executável são artefatos de build. As fontes que devem ser editadas durante o desenvolvimento são `lexer/lexer.l`, `parser/parser.y` e `src/main.c`.