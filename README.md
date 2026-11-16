## Etapa 0 — Preparando o ambiente

### Atividade: criar a página e executar o primeiro script

A página e o script inicial estão em `index.html` e [etapa-0.js](./etapa-0.js). A mensagem `Olá, JavaScript!` aparece no Console do navegador, não no conteúdo da página.

### Checkpoint — pausa e responda

1. **Em qual aba a mensagem apareceu?** Na aba Console das ferramentas do desenvolvedor.
2. **Por que o atributo `defer` é importante?** Ele faz o navegador executar o script depois de ler o HTML. Assim, os elementos da página já existem quando o JavaScript tenta encontrá-los ou alterá-los.
3. **O que acontece se o HTML apontar para `codigo.js`, mas o arquivo se chamar `script.js`?** O navegador não encontra o arquivo indicado e o script não é carregado; a mensagem não aparece e pode surgir um erro de carregamento no Console.

## Etapa 1 — O que é JavaScript

### Atividade: experimentos no Console

Os experimentos estão registrados em [etapa-1.js](./etapa-1.js).

| Expressão | Resultado |
| --- | --- |
| `2 + 3` | `5` |
| `"Web" + " I"` | `"Web I"` |
| `"5" + 3` | `"53"` |
| `"5" - 3` | `2` |
| `2 + 3 * 4` | `14` |
| `(2 + 3) * 4` | `20` |

### Checkpoint — pausa e responda

1. **Por que `"5" + 3` e `"5" - 3` dão resultados diferentes?** Com `+`, o JavaScript concatena se um dos operandos for texto, formando `"53"`. Com `-`, converte o texto `"5"` em número e calcula `5 - 3`, obtendo `2`.
2. **Por que `2 + 3 * 4` e `(2 + 3) * 4` são diferentes?** A multiplicação tem precedência sobre a soma: a primeira expressão vale `2 + 12 = 14`. Os parênteses fazem a soma ocorrer antes na segunda: `5 * 4 = 20`.

## Etapa 2 — Variáveis e tipos

### Atividade: declarar variáveis e observar os tipos

O exemplo está em [etapa-2.js](./etapa-2.js). A última linha tenta alterar uma constante e gera erro de propósito, como no exercício.

### Checkpoint — pausa e responda

1. **O que as quatro chamadas a `typeof` imprimem?** Respectivamente: `"string"`, `"number"`, `"boolean"` e `"undefined"`.
2. **Qual erro aparece ao tentar alterar `escola`? Por quê?** `TypeError: Assignment to constant variable`. `escola` foi declarada com `const`, portanto não pode receber outro valor.
3. **Quais nomes de variável são válidos?** `nota_final` e `$total` são válidos. `3nota` é inválido porque começa com número; `nota-final` é inválido porque contém hífen; `class` é inválido porque é uma palavra reservada.
4. **O que será impresso ao incrementar `idade`?** `16`, pois `15 + 1 = 16`.

## Etapa 3 — Operadores, conversão e texto com variáveis

### Atividade: executar cálculos e conversões

O código está em [etapa-3.js](./etapa-3.js).

### Checkpoint — pausa e responda

1. **Saída das chamadas a `console.log`, em ordem:**
   - `9 5 14`
   - `3.5`
   - `1`
   - `49`
   - `Olá, Ana! 7 dividido por 2 é 3.5.`
   - `8.5`
   - `"7.51"` (texto)
   - `NaN`
2. **Qual a diferença entre `Number("7.5") + 1` e `"7.5" + 1`? O que isso significa para campos de formulário?** `Number("7.5") + 1` converte o texto em número e resulta em `8.5`; `"7.5" + 1` concatena os textos e resulta em `"7.51"`. Como o valor de um campo chega como texto, é necessário convertê-lo com `Number()` antes de fazer operações aritméticas.
3. **Calcule `10 % 3`, `2 ** 3` e `10 / 4`:** `1`, `8` e `2.5`, respectivamente.

## Etapa 4 — Condicionais

### Atividade: testar temperaturas e comparações

O exemplo está no [script.js](./script.js). Com `temperatura = 25`, imprime `Agradável`.

### Checkpoint — pausa e responda

1. **Com temperatura igual a 20, qual mensagem aparece? E com 30? Por quê?** Com `20`, aparece `Agradável`: `temperatura >= 30` é falso e `temperatura >= 20` é verdadeiro. Com `30`, aparece `Calor`, pois a primeira condição já é verdadeira.
2. **Quais são as saídas das quatro últimas linhas? Por que recomendamos `===`?** As saídas são `true`, `false`, `true` e `false`. `==` converte tipos antes de comparar; `===` exige que valor e tipo sejam iguais, evitando comparações ambíguas.
3. **Condição para `nota` estar entre 0 e 10, inclusive:** `nota >= 0 && nota <= 10`.
