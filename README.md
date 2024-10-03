# Fundamentos-JavaScript

#### Minhas anotações

## Template String


Template strings são definidas usando crases **(`)** em vez de aspas simples **(')** ou duplas **(")**.

### Interpolação de Variáveis


```javacript
  const nome = "João";
  const idade = 25;
  const mensagem = `Meu nome é ${nome} e eu tenho ${idade} anos.`;
  console.log(mensagem); // "Meu nome é João e eu tenho 25 anos."
```

---

## Operador Ternário


O operador ternário em JavaScript é uma forma concisa de fazer uma verificação condicional. Ele funciona como um atalho para a estrutura if...else

#### Sintaxe

```javascript
  condição ? valorSeVerdadeiro : valorSeFalso;

```

- **Condição:** Uma expressão que será avaliada como verdadeira ou falsa.
- **Valor se verdadeiro:** O valor que será retornado se a condição for verdadeira.
- **Valor se falso:** O valor que será retornado se a condição for falsa.

```javascript
  let idade = 18;
  let podeDirigir = (idade >= 18) ? "Sim" : "Não";
  
  console.log(podeDirigir); // Saída: "Sim"

```

#### Explicação

- **Condição:** idade >= 18
- Se a condição for verdadeira, **podeDirigir** será **"Sim"**.
- Se for falsa, **podeDirigir** será **"Não"**.

---

## Math


O objeto Math em JavaScript é uma coleção de propriedades e métodos matemáticos que você pode usar para realizar cálculos. Aqui estão alguns dos principais recursos do objeto Math e como usá-los:

### Propriedades do Math

- **Math.PI:** O valor de π (pi), aproximadamente 3.14159.

- **Math.E:** O valor de e (base do logaritmo natural), aproximadamente 2.71828.

### Métodos do Math

- **Math.abs(x):** Retorna o valor absoluto de x.
```javascript
  console.log(Math.abs(-5)); // 5
```
- **Math.ceil(x):** Arredonda x para cima.
```javascript
  console.log(Math.ceil(4.2)); // 5
```
- **Math.floor(x):** Arredonda x para baixo.
```javascript
  console.log(Math.floor(4.7)); // 4
```
- **Math.round(x):** Arredonda x para o inteiro mais próximo.
```javascript
  console.log(Math.round(4.5)); // 5
```
- **Math.random():** Retorna um número pseudo-aleatório entre 0 (inclusive) e 1 (exclusivo).
```javascript
  console.log(Math.random()); // Um número aleatório entre 0 e 1
```
- **Math.max(...values):** Retorna o maior valor entre os argumentos.
```javascript
  console.log(Math.max(1, 2, 3)); // 3
```
- **Math.min(...values):** Retorna o menor valor entre os argumentos.
```javascript
  console.log(Math.min(1, 2, 3)); // 1
```
- **Math.pow(base, exponent):** Retorna a base elevada à potência do expoente.
```javascript
  console.log(Math.pow(2, 3)); // 8
```
- **Math.sqrt(x):** Retorna a raiz quadrada de x.
```javascript
  console.log(Math.sqrt(16)); // 4
```
- **Math.sin(x)**, **Math.cos(x)**, **Math.tan(x):** Retornam o seno, cosseno e tangente de x (em radianos).
```javascript
  console.log(Math.sin(Math.PI / 2)); // 1
  console.log(Math.cos(Math.PI));    // -1
```

---

## JSON


JSON é um formato baseado em pares de chave-valor. Por exemplo:

```javascript
{
  "nome": "João",
  "idade": 30,
  "email": "joao@example.com"
}
```

---

# Funções-JavaScript

#### Minhas anotações

## Função


Uma função é um bloco de código projetado para executar uma tarefa específica. Você pode chamar uma função sempre que precisar executar essa tarefa.

### Declaração de Funções

1. **Função Declarada (Function Declaration)**

```javascript

function saudacao(nome) {
    return `Olá, ${nome}!`;
}

console.log(saudacao("Maria")); // Saída: Olá, Maria!

```

2. **Função Anônima (Function Expression)**

```javascript

const somar = function(a, b) {
    return a + b;
};

console.log(somar(5, 3)); // Saída: 8

```

3. **Arrow Function (Função de seta)**

```javascript

const multiplicar = (x, y) => x * y;

console.log(multiplicar(4, 5)); // Saída: 20

```

### Parâmetros e Argumentos

- **Parâmetros** são as variáveis que você define na declaração da função.
- **Argumentos** são os valores que você passa para a função quando a chama.

```javascript

function exibirMensagem(mensagem) {
    console.log(mensagem);
}

exibirMensagem("Aprendendo JavaScript!"); // Saída: Aprendendo JavaScript!

```

### Retorno de Funções

Uma função pode retornar um valor usando a palavra-chave return. Quando uma função retorna um valor, você pode usá-lo na expressão que chamou a função.

```javascript

function calcularArea(base, altura) {
    return (base * altura) / 2;
}

const area = calcularArea(5, 10);
console.log(area); // Saída: 25

```

### Funções como Objetos

Em JavaScript, funções são objetos de primeira classe, o que significa que podem ser atribuídas a variáveis, passadas como argumentos e retornadas de outras funções.

```javascript

function executar(funcao) {
    funcao();
}

executar(() => console.log("Função executada!")); // Saída: Função executada!

```

### Funções Recursivas

Uma função pode chamar a si mesma. Isso é conhecido como recursão.

```javascript

function fatorial(n) {
    if (n === 0) {
        return 1;
    }
    return n * fatorial(n - 1);
}

console.log(fatorial(5)); // Saída: 120

```

---

# Orientação a Objeto-JavaScript

#### Minhas anotações

## Objeto


Um objeto é uma coleção de propriedades, onde cada propriedade é uma associação entre uma chave (ou nome) e um valor. Os valores podem ser de qualquer tipo, incluindo outros objetos, funções (que são chamadas de métodos quando associadas a um objeto) e tipos primitivos.

---

## Object.assign


O **Object.assign** é um método que é usado para copiar as propriedades de um ou mais objetos para um objeto de destino. Ele é muito útil para a criação de novos objetos a partir de objetos existentes, facilitando a combinação de propriedades e a criação de cópias de objetos.

#### Sintaxe

```javascript

Object.assign(destino, ...fontes);

```

- destino: O objeto que receberá as propriedades.
- ...fontes: Um ou mais objetos cujas propriedades serão copiadas para o objeto de destino.

#### Exemplo de uso

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const resultado = Object.assign({}, obj1, obj2);
console.log(resultado); // { a: 1, b: 3, c: 4 }

```

---

## Promise


Uma promessa é um objeto que representa a eventual conclusão ou falha de uma operação assíncrona e seu valor resultante. Ela pode estar em um dos seguintes estados:

- **Pendente (Pending)**: Estado inicial, quando a operação ainda não foi concluída.
- **Cumprida (Fulfilled)**: A operação foi concluída com sucesso.
- **Rejeitada (Rejected)**: A operação falhou.

---

## sessionStorage


é uma **API** de armazenamento web do JavaScript, que permite armazenar dados no navegador do usuário. A principal característica do sessionStorage é que ele mantém os dados apenas durante a sessão do navegador. Isso significa que os dados armazenados nele estão disponíveis enquanto a aba ou janela do navegador estiver aberta, mas serão perdidos assim que a aba for fechada.

---

## localStorage


O localStorage é outra **API** de armazenamento web do JavaScript, que permite armazenar dados no navegador do usuário de forma persistente. Ao contrário do sessionStorage, os dados armazenados no localStorage permanecem disponíveis mesmo após o fechamento da aba ou do navegador, até que sejam explicitamente removidos.

---
