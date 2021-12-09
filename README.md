# Compilador para a linguagem K-Script
Projeto de uma calculadora para a disciplina de Compiladores do Bacharelado em Ciência da Computação do IFCE.

### Pré-requisitos
- GCC
- Flex
- Bison

### Como compilar a aplicação

**Clone o repositório**

```
git clone https://github.com/karolinasena/projeto-final-compilador.git
```

 **Dentro da pasta do projeto, criar um arquivo *makefile* contendo o código abaixo:**
 
 Para o Linux:
```
all: compilador.l compilador.y
	flex -i calc.l
	bison calc.y
	gcc compilador.tab.c -o Compilador -lfl
	./Compilador
 ```
**No terminal, executar o comando:**

```
  make
```

## Uso da linguagem

**Início e fim do programa**
```
  ini
    ...
  end 
```

**Atribuição de valores às variáveis**
```
 int a = 10
 float b = 10.5
 string c = "Uma string"
```

**Ler variáveis**
```
 read(b) /* ler uma variável real */
 readstr(c) /* ler uma variável do tipo string */
```

**Escrever variáveis**
```
 write(b) /* escrever uma variável real */
 writes(c) /* escrever uma variável do tipo string */
```

**Estrutura condicional**
```
 if(a > b) {
  ...
 } else {
  ...
 }
```

**Estrutura de repetição**
```
 while(a > b) {  
      ...
 }
```

**Comentário de uma única linha**
```
  !! comentário de uma única linha
```

**Comentário de múltiplas linhas**
```
  !* comentário de
  múltiplas linhas *!
```
