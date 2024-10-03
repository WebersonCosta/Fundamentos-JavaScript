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

### Funções importantes da classe ***Object***

### Object.keys(obj)

A função **Object.keys(obj)** é um método em JavaScript que retorna um array contendo as chaves (propriedades enumeráveis) de um objeto

#### Sintaxe

```javascript

Object.keys(obj)

```

#### Retorno

Retorna um array contendo as chaves enumeráveis do objeto. Se o objeto não tiver propriedades enumeráveis, retorna um array vazio.

#### Exemplo

```javascript
const pessoa = {
    nome: 'João',
    idade: 30,
    cidade: 'São Paulo'
};

const chaves = Object.keys(pessoa);
console.log(chaves); // ['nome', 'idade', 'cidade']

```

### Object.values(obj)

A função **Object.values(obj)** é um método em JavaScript que retorna um array contendo os valores das propriedades enumeráveis de um objeto.

#### Sintaxe

```javascript

Object.values(obj)

```

#### Retorno

Retorna um array com os valores das propriedades enumeráveis do objeto. Se o objeto não tiver propriedades enumeráveis, retorna um array vazio.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30,
    cidade: 'São Paulo'
};

const valores = Object.values(pessoa);
console.log(valores); // ['João', 30, 'São Paulo']

```

### Object.entries(obj)

A função **Object.entries(obj)** é um método em JavaScript que retorna um array de arrays, onde cada sub-array contém um par chave-valor de um objeto.

#### Sintaxe

```javascript

Object.entries(obj)

```

#### Retorno

Retorna um array de arrays, onde cada sub-array contém dois elementos: a chave e o valor correspondente. Se o objeto não tiver propriedades enumeráveis, retorna um array vazio.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30,
    cidade: 'São Paulo'
};

const entradas = Object.entries(pessoa);
console.log(entradas); 
// [['nome', 'João'], ['idade', 30], ['cidade', 'São Paulo']]

```

### Object.assign(target, ...sources)

O **Object.assign** é um método que é usado para copiar as propriedades de um ou mais objetos para um objeto de destino. Ele é muito útil para a criação de novos objetos a partir de objetos existentes, facilitando a combinação de propriedades e a criação de cópias de objetos.

#### Sintaxe

```javascript

Object.assign(destino, ...fontes);

```

1. destino: O objeto que receberá as propriedades.
2. ...fontes: Um ou mais objetos cujas propriedades serão copiadas para o objeto de destino.

#### Exemplo

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const resultado = Object.assign({}, obj1, obj2);
console.log(resultado); // { a: 1, b: 3, c: 4 }

```

### Object.freeze(obj)

A função **Object.freeze(obj)** é um método em JavaScript que congela um objeto, tornando-o imutável. Isso significa que você não pode adicionar, remover ou modificar suas propriedades depois que o objeto foi congelado.

#### Sintaxe

```javascript

Object.freeze(obj)

```
#### Comportamento

  1. **Imutabilidade:** Depois de congelado, um objeto não pode ter novas propriedades adicionadas, propriedades existentes não podem ser removidas ou modificadas (mesmo que suas propriedades sejam objetos).
  2. **Propriedades Não Enumeráveis:** O método não afeta as propriedades não enumeráveis de um objeto. Se o objeto já tiver propriedades não enumeráveis, elas permanecerão inalteradas.
  3. **Níveis de Congelamento:** Apenas o objeto em si é congelado. Se ele contém objetos aninhados, essas propriedades aninhadas ainda podem ser alteradas a menos que também sejam congeladas.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30
};

Object.freeze(pessoa);

pessoa.idade = 31; // Não fará nada
pessoa.cidade = 'São Paulo'; // Não fará nada
delete pessoa.nome; // Não fará nada

console.log(pessoa); // { nome: 'João', idade: 30 }

```

### Object.seal(obj)

A **função Object.seal(obj)** é um método em JavaScript que "sele" um objeto, permitindo que suas propriedades existentes sejam modificadas, mas impedindo que novas propriedades sejam adicionadas ou que propriedades existentes sejam removidas. 

#### Sintaxe

```javascript

Object.seal(obj)

```

#### Comportamento

1. **Imutabilidade Estrutural:** Depois que um objeto é selado, você não pode adicionar novas propriedades ou remover as existentes. No entanto, você ainda pode modificar os valores das propriedades existentes, desde que elas sejam enumeráveis
2. **Propriedades Não Enumeráveis:** O método não afeta as propriedades não enumeráveis de um objeto. Se o objeto já tiver propriedades não enumeráveis, elas permanecerão inalteradas.
3. **Propriedades Existentes:** Você pode modificar as propriedades existentes, mesmo que estejam seladas.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30
};

Object.seal(pessoa);

pessoa.idade = 31; // Permite a modificação
pessoa.cidade = 'São Paulo'; // Não permite a adição
delete pessoa.nome; // Não permite a remoção

console.log(pessoa); // { nome: 'João', idade: 31 }

```

### Object.getOwnPropertyNames(obj)

A **função Object.getOwnPropertyNames(obj)** é um método em JavaScript que retorna um array contendo os nomes (chaves) de todas as propriedades de um objeto, tanto as enumeráveis quanto as não enumeráveis. 

```javascript

Object.getOwnPropertyNames(obj)

```

#### Retorno

Retorna um array com os nomes de todas as propriedades do objeto. Se o objeto não tiver propriedades, retorna um array vazio.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30
};

Object.defineProperty(pessoa, 'cpf', {
    value: '123.456.789-00',
    enumerable: false // Não enumerável
});

const propriedades = Object.getOwnPropertyNames(pessoa);
console.log(propriedades); // ['nome', 'idade', 'cpf']

```
  
### Object.getPrototypeOf(obj)

A função Object.getPrototypeOf(obj) é um método em JavaScript que retorna o protótipo do objeto especificado. O protótipo é o objeto a partir do qual o objeto dado herda suas propriedades e métodos.

#### Sintaxe

```javascript

Object.getPrototypeOf(obj)

```
#### Retorno

Retorna o protótipo do objeto especificado. Se o objeto não tiver um protótipo (como um objeto criado com Object.create(null)), o método retornará null.

#### Exemplo

```javascript

const pessoa = {
    nome: 'João',
    idade: 30
};

const prototipo = Object.getPrototypeOf(pessoa);
console.log(prototipo); // { ... } (prototipo padrão do objeto)

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
