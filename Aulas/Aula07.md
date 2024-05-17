# Aula 7: Operadores Lógicos e Expressões Lógicas

### Operadores Lógicos:

Os operadores lógicos são utilizados para combinar ou negar expressões lógicas.Na linguagem C, os principais operadores lógicos são:
- E lógico (&&): Retorna verdadeiro se ambas as expressões forem verdadeiras.

| A | && | B |
|   :---:  |   :---:  |   :---:  |
| V | V | V |
| V | F | F |
| F | F | V |
| F | F | F |

A proposição lógica "E" (&&) é verdadeira apenas quando todas as proposições são verdadeiras. Veja alguns exemplos:

Exemplo 1:
Proposição 1: Está chovendo.
Proposição 2: Está ventando.
Proposição lógica: Está chovendo && Está ventando.
Neste caso, a proposição lógica seria verdadeira apenas se as duas condições (está chovendo e está ventando) fossem verdadeiras.

Exemplo 2:
Proposição 1: Hoje é segunda-feira.
Proposição 2: Hoje é feriado.
Proposição lógica: Hoje é segunda-feira && Hoje é feriado.
Neste caso, a proposição lógica seria falsa, pois nem todas as condições são verdadeiras.

- OU lógico (| |): Retorna verdadeiro se pelo menos uma das expressões for verdadeira.

| A | \| \| | B |
|   :---:  |   :---:  |   :---:  |
| V | V | V |
| V | V | F |
| F | V | V |
| F | F | F |

A proposição lógica "OU" (||) é verdadeira quando pelo menos uma das proposições é verdadeira. Veja alguns exemplos:

Exemplo 1:
Proposição 1: Está chovendo.
Proposição 2: Está ventando.
Proposição lógica: Está chovendo || Está ventando.
Neste caso, a proposição lógica seria verdadeira se pelo menos uma das condições (está chovendo ou está ventando) fosse verdadeira.

Exemplo 2:
Proposição 1: Hoje é segunda-feira.
Proposição 2: Hoje é sábado.
Proposição lógica: Hoje é segunda-feira || Hoje é sábado.
Neste caso, a proposição lógica seria falsa, pois apenas uma das condições é verdadeira.

- NÃO lógico (!): Inverte o valor da expressão, se for verdadeira, torna-se falsa e vice-versa.

| ! | A |
|   :---:  |   :---:  |
| F | V |
| V | F |

Proposição original: Está chovendo.
Proposição de negação: ¬(Está chovendo).

Neste caso, a proposição de negação seria verdadeira se a proposição original "Está chovendo" fosse falsa, e falsa se a proposição original fosse verdadeira.

Então, podemos ter os seguintes cenários:

Se está chovendo (proposição original verdadeira), a negação (¬(Está chovendo)) seria falsa.
Se não está chovendo (proposição original falsa), a negação (¬(Está chovendo)) seria verdadeira.

Outro exemplo:
Proposição original: Hoje é segunda-feira.
Proposição de negação: ¬(Hoje é segunda-feira).

Neste caso, a proposição de negação seria verdadeira se a proposição original "Hoje é segunda-feira" fosse falsa, e falsa se a proposição original fosse verdadeira.

### Expressões Lógicas:

As expressões lógicas são combinações de valores e operadores lógicos que resultam em um valor verdadeiro ou falso (booleano). Podemos utilizar operadores de comparação para criar expressões lógicas, tais como:
- Igual a (==): Verifica se dois valores são iguais.
- Diferente de (!=): Verifica se dois valores são diferentes.
- Maior que (>), Maior ou igual a (>=), Menor que (<), Menor ou igual a (<=): Comparação numérica.
#### Exemplo de expressão lógica:
``` C
idade > 18 && salario < 1000
dia >= 18 || mês == 4
altura != 1.60
```
### Estrutura de Decisão:

- A estrutura de decisão permite que o programa tome diferentes caminhos com base nas condições estabelecidas. Na linguagem C, a estrutura de decisão mais comum é o "if-else", que avalia uma expressão lógica e executa um bloco de código caso a condição seja verdadeira e outro bloco de código caso a condição seja falsa.

#### Exemplo:
``` C
if (idade >= 18) {
    printf("Você é maior de idade.\n");
} else {
    printf("Você é menor de idade.\n");
}
```

### Estrutura de Decisão Encadeada:

É possível encadear múltiplas estruturas "if-else" para lidar com diferentes condições.

#### Exemplo:

``` C
if (idade < 13) {
    printf("Você é uma criança.\n");
} else if (idade < 18) {
    printf("Você é um adolescente.\n");
} else {
    printf("Você é um adulto.\n");
}
```

### Operador Ternário:

O operador ternário é uma forma abreviada de escrever uma estrutura de decisão simples.
``` C
Sintaxe: expressão ? valor_verdadeiro : valor_falso
```
#### Exemplo:
``` C
printf((idade >= 18) ? "Você é maior de idade.\n" : "Você é menor de idade.\n");
```
