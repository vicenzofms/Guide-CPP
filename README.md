# **Guia Para Programação Básica C++**
#### (Assumindo que você sabe algorítimo)
Vamos te guiar para a programação básica de C++, uma linguagem muito poderosa! Bora lá programadores :D
## **Primeiro Script C++**
O seu primeiro código será muito simples. Uma mensagem de "Olá Mundo!" na tela.
Para começar o seu código, vamos importar a biblioteca `bits/stdc++.h` para obtermos acesso a coisas básicas do C++, logo após iremos utilizar a `namespace std` para facilitar o trabalho, finalmente, criaremos a função `main`, ou seja, a função principal, a que é executada pelo computador no início do seu programa.
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    return 0;
}
```
Seu código deve estar assim ao final.
Devo acresentar que onde escrevemos `//` no programa estamos dizendo que tudo que está na frente será um "comentário", algo que o computador não lerá como código. Utilizamos comentários para explicar o programa.
Agora vamos mostrar o nosso texto na tela, utilizaremos o comando `cout` para isso, sua sintaxe implementada na função `main` é:
```cpp
int main(){
    cout << "Olá Mundo! :D" << endl; // essa é a nova linha de código
    return 0;
}
```
Podemos ver que depois do texto, implementamos um `<< endl;`para que quebremos a linha digitada pelo usuário. Terminamos a linha com um `;` para indicar que aquela linha acabou.
Se executarmos o scirpt acima, teremos esse **output**:
> Olá Mundo! :D

Exatamente o que queriamos! Parabéns!
##### **Para criar e compilar seus própios códigos veja o guia anexado a esse (Guia de Compilar)[guide_to_compile_cpp.md]! É muito importante que execute os passos ditos lá para acompanhar e escrever seus própios códigos durante o percurso deste guia. Não se aprende somente vendo, é necessário praticar!**

## **Tipos de variáveis**
Aqui vamos ver a lista de alguns tipos primitivos de variáveis comuns em C++.
| Tipo | Descrição | Exemplos | 
| ------ | ----------- | ------ |
| int   | Número inteiro | **30, 60, -3, 0...** |
| float | Números fracionários. | **7, -5.6, 1.2, 500, 0.3** |
| string    | Cadeia de carácteres | **"Vicenzo", "Jogo de Computador", "C++", "Aprender é legal! :p"** |
| char | Um caractere. | **'A', '[', 'v', '+', 'b'**|
| bool | Booleano | **true, false** |

## **Operadores Comuns Em C++**
Aqui vamos ver a lista dos operadores mais importantes do C++
| Operadores de Comparação | Descrição | Exemplos | 
| ------ | ----------- | ------ |
| `==` | Igual à | `if ( x == y ){...}` |
| `!=` | Diferente de | `if ( x != y ){...}` |
| `&&` | e -> somente se duas condições são verdadeiras | `if ( (condicao1) && (condicao2) ){...}` |
| ` \|\| ` |ou -> se uma das condições for verdadeira | `if ( (condicao1) \|\| (condicao2) ){...}` |

| Operadores de Atribuição | Descrição | Exemplos | 
| ------ | ----------- | ------ |
| =  | Recebe | `x = y`  |
| += | Soma e depois atribuí | `x += y` |
| +- | Subtraí e depois atribuí | `x +- y` |
| /- | Divide e depois atribuí | `x /- y` |
| *- | Multiplica e depois atribuí | `x *- y` |
| ++ | Soma 1 e atribuí | `x++` |
| -- | Subtraí 1 e atribuí | `x--` |

| Operadores Aritméticos | Descrição | Exemplos | 
| ------ | ----------- | ------ |
| +   | Soma | x + y  |
| - | Subtração | x - y |
| /    | Divisão | x / y |
| * | Multiplicação | x * y |

## **Pegando o Input do Usuário**
Digamos que você queira fazer um programa que receba a idade do usuário e depois diga algo legal.
Para isso utilizaremos o `cin`, um comando irmão do `cout` (que já vimos neste guia). Ele pega um valor digitado pelo usuário e o guarda em uma **variável**, para que possamos utilizar esse valor mais tarde.
Primeiramente, você digitaria o início do programa, e depois cria uma variável que armazenará o valor da idade do usuário. Ela será do tipo **inteiro**. Segue o código:
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    int idade = 0; // inicializa a váriavél com valor 0
    return 0;
}
```
Agora que temos a variável em mãos, podemos utilizar o `cin` para atribuir o valor digitado pelo usuário a ela.
```cpp
int main(){
    int idade = 0; // inicializa a váriavél com valor 0
    cin >> idade;
    return 0;
}
```
Vemos que o símbolo mudou, agora estamos usando `>>`, para "jogar" o valor digitado na variável *idade*. Implementando a linha para mostrar uma mensagem com essa estrutura: `Agora eu sei que você tem {variável idade} anos`, ficamos com essa função:
```cpp
int main(){
    int idade = 0; // inicializa a váriavél com valor 0
    cin >> idade;
    cout << "Agora eu sei que você tem " << idade << " anos." << endl;
    return 0;
}
```

#### Alerta! Estamos mostrando durante o desenvolvimento do código somente a função `main`, não se esqueça do resto!

Observamos o uso do operador `<<` para concatenar termos na linha de código da mensagem.
Quando executarmos, seremos requisitados uma idade, vamos digitar 15:
> 15

E teremos esse output:
> Agora eu sei que você tem 15 anos.

Prontinho, seu programa está funcionando perfeitamente!

## **Utilizando Condições**
Esse é um recurso importantíssimo na programação! Vamos lhe mostrar como é sua sintaxe em C++.
### If (se)
Criaremos um programa que receberá um valor `nome` (variável string) e irá verificar se o nome é igual a "Vicenzo", se ele for, o programa fará um elogio (hehe), se não ele continuará normalmente. Primeiramente inicamos o programa e a(s) variavél(is) necessária(s).
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    string nome = ""; // inicia a variável `nome` vazia
    cout << "Digite seu nome: "; // diz para o usuário que ele precisa digitar sua idade
    cin >> nome; // recebe o valor do nome e o coloca na variável `nome`
    
    return 0;
}
```
Agora vamos utilizar a sintaxe do `if (verificação)` (se) para fazer a nossa condição, e caso ela retorne verdadeira execute um bloco de código determinado por chaves `{` e  `}`.
```cpp
if (nome == "Vicenzo"){ // codição dentro dos parênteses
    cout << "Seu nome é muito bonito!" << endl; // elogio que só acontece se for verdade
}
```
Implementando esse pedaço de código na nossa função `main`, vamos adicionar uma última linha de código, agradeçendo o usuário por digitar o nome.
```cpp
cout << "Obrigado por digitar " << nome << "!" << endl;
```
Vou mostrar agroa o código todo no final para não restar nenhuma dúvida de como ele foi estruturado! Compare com o seu e veja se conseguiu seguir o passo a passo.
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    string nome = ""; // inicia a variável `nome` vazia
    cout << "Digite seu nome: "; // diz para o usuário que ele precisa digitar sua idade
    cin >> nome; // recebe o valor do nome e o coloca na variável `nome`
    if (nome == "Vicenzo"){ // codição dentro dos parênteses
        cout << "Seu nome é muito bonito!" << endl; // elogio que só acontece se for verdade
    }
    cout << "Obrigado por digitar " << nome << "!" << endl;
    return 0;
}
```
Caso o nome não seja "Vicenzo" o programa só agradeçerá, porém se for, ele irá fazer um elogio. Veja os dois casos:
> Digite seu nome: **Rian**
Obrigado por digitar Rian!

>Digite seu nome: **Vicenzo**
Seu nome é muito bonito!
Obrigado por digitar Vicenzo!

### Else (se não)
Vamos utilizar o programa do exemplo anterior e aplicar o `else` (se não), iremos fazer com que se o nome não for "Vicenzo" o programa dizer: `É uma pena. ;-;`. Para isso vamos voltar na condição e acresentar após as aspas o comando `else` e outro bloco de código, que será executado caso a condição seja falsa.
```cpp
if (nome == "Vicenzo"){
    cout << "Seu nome é muito bonito!" << endl;
} else { // se o nome não for "Vicenzo"
    cout << "É uma pena. ;-;" << endl;
}
```
Aplicando isso no código completo ficamos com esse script:
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    string nome = ""; // inicia a variável `nome` vazia
    cout << "Digite seu nome: "; // diz para o usuário que ele precisa digitar sua idade
    cin >> nome; // recebe o valor do nome e o coloca na variável `nome`
    if (nome == "Vicenzo"){
    cout << "Seu nome é muito bonito!" << endl;
    } else { // se o nome não for "Vicenzo"
        cout << "É uma pena. ;-;" << endl;
    }   
    cout << "Obrigado por digitar " << nome << "!" << endl;
    return 0;
}
```
Vamos executar duas vezes e ver os 2 resultados possíveis agora:
> Digite seu nome: **Enzo**
É uma pena. ;-;
Obrigado por digitar Enzo!

>Digite seu nome: **Vicenzo**
Seu nome é muito bonito!
Obrigado por digitar Vicenzo!

### Else  If (se não se)
Agora vamos melhorar o último código. Vamos elogiar mais de um nome, não somente `Vicenzo`, também queremos elogiar caso o usuário tenha o nome `Cleiton` ou `Rogério`. Usaremos a estrutura `else if (nova condição)` para isso. Vamos também manter o `else` no caso do nome não ser nenhum dos três.
```cpp
if (nome == "Vicenzo"){
    cout << "Seu nome é muito bonito!" << endl;
} else if (nome == "Cleiton"){ // se o nome for "Cleiton"
    cout << "Seu nome é lindo!" << endl;
} else if (nome == "Rogério"){ // se o nome for "Rogério"
    cout << "Seu nome é maravilhoso!" << endl;
} else { // nome não é nenhum dos três
    cout << "É uma pena. ;-;" << endl;
}
```
Colocando a nossas novas condições no código, conseguimos:
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    string nome = ""; // inicia a variável `nome` vazia
    cout << "Digite seu nome: "; // diz para o usuário que ele precisa digitar sua idade
    cin >> nome; // recebe o valor do nome e o coloca na variável `nome`
    if (nome == "Vicenzo"){
        cout << "Seu nome é muito bonito!" << endl;
    } else if (nome == "Cleiton"){ 
        cout << "Seu nome é lindo!" << endl;
    } else if (nome == "Rogério"){
        cout << "Seu nome é maravilhoso!" << endl;
    } else {
        cout << "É uma pena. ;-;" << endl;
    } 
    cout << "Obrigado por digitar " << nome << "!" << endl;
    return 0;
}
```
Vamos executar quatro vezes e ver os 4 resultados possíveis agora:
> Digite seu nome: **Rogério**
Seu nome é maravilhoso!
Obrigado por digitar Rogério!

> Digite seu nome: **Cleiton**
Seu nome é lindo!
Obrigado por digitar Cleiton!

>Digite seu nome: **Vicenzo**
Seu nome é muito bonito!
Obrigado por digitar Vicenzo!

>Digite seu nome: **Alonso**
É uma pena. ;-;
Obrigado por digitar Alonso!

Aqui finalizamos a saga dos nomes! :P
## **Compreendendo e criando Arrays**
Arrays são variavéis que contém diversos valores. Parece estranho né? Uma variavél com várias variavéis. Porém você se acostuma rápidamente. Acompanhe comigo.
Vamos criar um array de nome: `numeros` e vamos guardar os valores: `5  8  9  11 -13` nele. Precisamos primeiramente do tipo do nosso array, neste caso, **inteiro**. Segundamente vamos descobrir o tamanho do nosso array, nessa situação, o seu tamanho é **5**. Agora que sabemos todos as informações que precisamos, vamos criar o array em C++:
```cpp
int numeros[5];
```
Pode-se ver que declarei o tamanho do Array entre os `[]`. Agora podemos atribuir os valores que citei em suas devidas posições, só que para isso temos que entender como são enumeradas as posições. Elas vão de `0` a `N-1` onde `N` é o tamanho do Array. Com o nosso Array, ele vai de 0 a 4 (0, 1, 2, 3, 4). Para acessarmos um valor dentro do Array utilizamos a seguinte sintaxe: `nomeDoArray[indice]`, onde índice é a posição do valor que queremos pegar. Agora podemos atribuir os valores que queremos no nosso Array.
```cpp
numeros[0] = 5; // primeira posição
numeros[1] = 8; // segunda posição
numeros[2] = 9; // terceira posição
numeros[3] = 11; // quarta posição
numeros[4] = -13; // quinta posição
```
Representação do array em tabela:
| Posição | Valor |
|-|-|
| 0 | 5 |
| 1 | 8 |
| 2 | 9 |
| 3 | 11 |
| 4 | 13 |

Nosso Array está pronto. Agora se formos dar `cout` em alguma das posições válidas veriamos o seu valor. Veja:
```cpp
cout << "Terceira Posição: " << numeros[2] << endl;
```
Output:
> 9

Isso funcionaria para todas as posições, mas vamos manter só isso por agora. E como eu fiz em todos os tópicos, código final ficará disponível agora para você conferir o que você fez:
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    int numeros[5];
    numeros[0] = 5; // primeira posição
    numeros[1] = 8; // segunda posição
    numeros[2] = 9; // terceira posição
    numeros[3] = 11; // quarta posição
    numeros[4] = -13; // quinta posição
    
    cout << "Terceira Posição: " << numeros[2] << endl;
    
    return 0;
}
```

## **Estruturas de Repetição Importantes**
São importantíssimas para resolução de problemas e criação de **diversos** programas. Não cansarei de mencionar a necessidade de compreende-las e saber usá-las de maneira inteligente e correta.
### While (enquanto)
Usamos ela para repetir um determinado bloco de código enquanto uma condição não for verdadeira. Vamos entender melhor com um exemplo. Criaremos uma variável `contador` e a utilizaremos para contar até um determinado número `X`. Vamos então, inicializar o programa com essas duas variáveis.
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    int contador = 0, X = 0; // declara as variáveis
    cout << "Digite X: ";
    cin >> X;
    
    return 0;
}
```
Podemos ver também, que podemos declarar várias variáveis do mesmo tipo na mesma linha, como acima.
Agora vamos criar a estrura de repetição que irá contar até X.
```cpp
while(contador < X){
    contador++; // incrementa o valor da variável em 1
    cout << contador << endl;
}
```
Somente assim, conseguimos o nosso contado. Vou mostrar o código completo e depois um exemplo.
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    int contador = 0, X = 0; // declara as variáveis
    cout << "Digite X: ";
    cin >> X;
    while(contador < X){
        contador++; // incrementa o valor da variável em 1
        cout << contador << endl;
    }
    return 0;
}
```
Exemplo:
> Digite X: **10**
1
2
3
4
5
6
7
8
9
10

### For (para)
Essa é a estrutura mais utilizada. Confie em mim, se você aprender a utilizar essa estrutura de repetição sua vida ficará 10 vezes mais fácil. Ela funciona baseada em uma **variável de controle**. Ou seja, o loop vai funcionar baseado nela. Veja um exemplo de sintaxe que funcionaria igual o exemplo do While (contar até 10).
```cpp
for (int contador = 1; contador <= 10; contador++){
    cout << contador << endl;
}
```
Aplicando esse loop no código mais e substituindo 10 por X, vamos obter esse código final:
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    int X = 0; // declara as variáveis
    cout << "Digite X: ";
    cin >> X;
    for (int contador = 1; contador <= X; contador++){
        cout << contador << endl;
    }
    return 0;
}
```
Também se observa que eu removi a variável `contador` da declaração no início do código. Isso se dá ao fato de que agora, a variável `contador` é local e só existe dentro do bloco de código do `for`. Atenção! Com o `for` o nome de variável de controle mais comum é `i`, então não se assuste quando vê-lo.

## **Testando o que aprendeu!**
Parabéns! Você chegou no final deste guia básico de C++. Agora, eu vou lhe passar um exercício que englobará tudo que aprendemos e tente resolvê-lo por si só. Ele não é fácil para iniciantes, então se esforçe. Depois de fazer/tentar, confira seu código com a solução do problema. Lembre-se, seu aprendizado em C++ não acaba aqui! Continue explorando a linguagem e fazendo projetos, sejam eles pequenos ou grandes, para sempre aprimorar seu conhecimento e se tornar cada vez mais um melhor programador! :D

### **Exercício**:
Construa um programa que receberá um array de números inteiros e verifique se um determinado número está presente nele.

As suas linhas de entrada serão compostas por um número T, que será o tamanho do array, depois T linhas seguintes com os valores do array, e por último o número X que você deve verificar se está presente.

A linha de saída deve conter uma única palavra. **"Sim"** caso o número estiver presente e **"Não"** caso ele não esteja presente.

#### Exemplo 1:

Entrada
> Digite T: **5**
Digite a posição 0: 1
Digite a posição 1: 15
Digite a posição 2: 23
Digite a posição 3: 4
Digite a posição 4: 73
Digite X: 4

Saída
> Sim

#### Exemplo 2:

Entrada
> Digite T: **7**
Digite a posição 0: 1
Digite a posição 1: 15
Digite a posição 2: 23
Digite a posição 3: 4
Digite a posição 4: 73
Digite a posição 5: -84
Digite a posição 6: 29
Digite X: 9

Saída
> Não

Tente resolver por si só, eu tenho certeza que com tudo que aprendeu ao longo deste guia, você consegue resolver esse exercício. O código que o resolve está abaixo. Não olhe ele antes de tentar resolver. Essa é uma boa oportunidade para colocar seu cérebro para trabalhar! Boa sorte programador! :D

**Resposta:**
```cpp
#include <bits/stdc++.h>
using namespace std;
int main(){
    
    int T = 0, X = 0; // cria as variáveis
    bool achou = false; // cria a variável booleana de se o número já foi achado
    cin >> T; // recebe o input de T
    int arrayDeNumeros[T]; // cria o arrayDeNumeros com tamanho T
    for (int i = 0; i < T; i++){ // percorre o arrayDeNumeros
        cin >> arrayDeNumeros[i]; // recebe o input e coloca no arrayDeNumeros no índice "i"
    }
    cin >> X; // recebe o input de X
    
    for (int k = 0; k < T; k++){ // percorre o arrayDeNumeros
        if (arrayDeNumeros[k] == X){ // se o arrayDeNumeros no índice K (variavel de controle) == X
            achou = true; // o número foi achado
        }
    }
    
    // se ele terminar o loop for acima e o número estiver presente, a variável "achou" será verdadeira
    // se a variável "achou" ainda estiver falsa o número não está presente
    
    if (achou){
        cout << "Sim" << endl;
    } else {
        cout << "Não" << endl;
    }
    
    return 0;
}
```

## **Término** 
Eu espero que tenha te ajudado a se tornar um programador de C++ melhor do que você era antes, se gostou me de um feedback no e-mail (vicenzofms @ gmail .com). Obrigado por acompanhar o guia!

#### Autor: Vicenzo Fonseca de Mello Souza


