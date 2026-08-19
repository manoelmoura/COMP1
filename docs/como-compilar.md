# Como compilar

## Dependências

Em Debian, Ubuntu ou WSL:

```bash
sudo apt-get update
sudo apt-get install flex bison gcc
```

No Windows, o caminho mais simples é usar o MSYS2 com o ambiente MinGW64 e instalar `flex`, `bison` e `gcc` pelo gerenciador de pacotes.

## Gerar e compilar

Na raiz do repositório:

```bash
bison -d parser/parser.y -o parser.tab.c
flex -o lex.yy.c lexer/lexer.l
gcc parser.tab.c lex.yy.c -o compilador
```

No MSYS2, se a biblioteca do Flex for necessária:

```bash
gcc parser.tab.c lex.yy.c -o compilador -lfl
```

## Executar

```bash
echo "12 + 3 * (4 - 1)" | ./compilador
```

Uma entrada inválida, como `12 + )`, passa pelo mesmo pipeline e produz uma mensagem de erro sintático.

## Visualizar esta documentação

Instale as dependências do site e inicie o servidor local:

```bash
python -m pip install -r docs/requirements.txt
mkdocs serve
```

O site ficará disponível em `http://127.0.0.1:8000`.