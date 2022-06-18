# Solidity

<img src="https://user-images.githubusercontent.com/16539849/173656651-a46df615-8ec3-43fd-9619-98647a6d2bd2.png" />

# O que é `Solidity`?
- Solidity é uma linguagem OO, de alto nível (OOP, High-level language) para implementação de smart contracts. Ele é projeto para atingir o Ethereum Virtual Machine (EVM).
- É estaticamente tipado, suporta heranças, bibliotecas e tipos complexos definos pelo usuários entre outros recursos.

# Construindo com Solidity

## Inicializando smart contracts

```sol
// Defina a versão do compilador que você vai usar.
pragma solidity ^0.8.10;

// Começe criando um contrato chamado HelloWorld

contract HelloWorld {...}
```

# Variáveis e tipos

Existem 3 tipos de variáveis na Solidity.

- Local
Declarada dentro da função e não é armazenada na blockchain.

- State
Declarado fora da função para manter o estado do smart contract e é armazenado na blockchain.

- Global
Fornece informações sobre a blockchain. Eles são injetados pela Ethereum Virtual Machine em runtime. 
Inclui coisas como remetentes de transações, block timestamp, block hash, etc.

O escopo da variável é definida onde elas são declaradas, não seu valor. Definir o valor de uma variável local para uma variável global não a torna uma variável global, pois ainda é acessível apenas dentro do seu escopo local.

```
- uint = (sem sinal) -> inteiros não negativos
- uint8 (128bits?) -> varia de 0 a 2 ** (8 - 1)
- uint256 -> varia de 0 a 2 ** (256 - 1)
```
- public significa que essas variáveis podem ser acessadas internamente e lidas pelo meio externo
```
uint8 public u8 = 10;
uint public u256 = 600;
uint public u = 1230; // default = uint256
```

Números negativos são permitidos por numeros inteiros: ex:
```
- int256 varia de -2 ** 255 a 2 ** 255-1
```
```
int public i = -123; // int é mesma coisa que int256
```

// address significa um endereço ethereum
```
address public addr = 0xCA35b7d915458EF540aDe6068dFe2F44E8fa733c;
```
// bool significa booleano
```
bool public defaultBoo1 = false;
```
```
// Valores padrões 
// Variáveis não definidas tem valores padrões na solidity.
bool public defaultBoo2; // false
uint public defaultUint; // 0
int public defaultInt; // 0
address public defaultAddr; // 0x0000000000000000000000000000000000000000
```
```
function doSomething() public {
    /*
    ******** Variável local **********
    */
    uint ui = 456;

    /*
    ******** Global variables **********
    */

    
    // "block.timestamp" nos diz qual o timestamp para o bloco atual.

    // "msg.sender" nos diz qual endereço chamou a função doSomething

    /************/
    
    
    // Current block timestamp
    uint timestamp = block.timestamp; 

    // address of the caller
    address sender = msg.sender; 
}
```

# Funções, Loops e If/else

```
// Nome da função é set. Ela recebe um uint e seta the a variável de estado num.

// Ela é declarada publicamente, o que significa que pode ser chamada dentro da função e externamente a ela.
  
function set(uint _num) public {
  num = _num;
}

  
// Nome da função é get. ela retorna o valor de num.

// É declarado como uma função de visualização "view", que significa que ela não vai mudar o estado de nenhuma variável. funções "view" na solidity não requerem "gás" 
Gas = taxa = que são especificadas em gwei.

function get() public view returns (uint) {
    return num;
}
```


```
/*Nome da função é foo. Ela recebe um uint como argumento e retorna um uint. ela compara o valor de X usando if/else*/

function foo(uint x) public return (uint) {
  if (x < 10) {
    return 0;
  } else if (x < 20) {
    return 1;
  } else {
    return 2;
  }
}
```

```
// Nome da função é loop e ela executa um loop até 10.

function loop() public {
  for (uint i = 0; i < 10; i++) {
    if (i == 3) {
      // Skip
      continue;
    }

    if (i == 5) {
      // Exit
      break;
    }
  }
}
```

# Arryas, Strings

```
// Declara uma função a qual é publica.
string public greet = "Hello World";

/*
* Varias maneiras de inicilizar um array, array inicializados aqui são considerados variáveis de estados que são armazenadas no blockchain.

!"Ela são chamadas de variáveis de armazenamento"

uint[] public arr;
uint[] public arr2 = [1, 2, 3];
// Array de inteiros com tamanho 10!!
uint[10] public myFixedSizeArr;

// Retorna o valor no indice que passarmos por argumento do array.

function get(uint i) public view return (uint) {
  return arr[i]
}

Solidity também retorna o array inteiro.

Essa função gets é chamada com um array uint[] em memória.

memory -> o valor é armazenado somente na memória, e não na blockchain e só existe durante o tempo em que a função é executada.

"Memory variables" e "Storage Variables" -> podem ser pensados com semelhanças a RAM vs HD.

"Memory variables" existe temporariamente, durante o tempo da execução da função, enquanto as "Storage Variables" são persistentes através de chamadas de funções para o tempo de vida do contrato.

// Aqui um exemplo onde temos um array em que precisamos somente dele durante a execução da função e assim é declarado como uma variável de memória.

function getArr(uint[] memory _arr) public view return (uint[] memory) {
  return _arr;
}

// Esta função retorna uma string em memory, e isso funciona porque internamente a string é tratada como array, aqui é uma string que é só precisamos dela durante o tempo da execução da função.

function foo public returns (string memory) {
  return "C";
}

// aumenta o tamanho do array em 1
arr.push(i);

// diminui o tamanho do array em 1
arr.pop();

// pega o tamanho do array
uint length = arr.length;

uint index = 1
delete arr2[index]; // delete arr2[1];

// cria um array em memória, somente pode ser feito criando com tamanho fixo.

uint[] memory a = new uint[](5);

// cria uma string em memoria
string memori hi = "hi";
*/
```

