# Java

## Scanner

> A entrada do teclado usando Scanner requer a seguinte importação: 

``` java
import java.util.Scanner;
```

Para inicializar um Scanner o defina assim: 

``` java
Scanner scanner = new Scanner(System.in);
```
> System.in é usado pelo scanner para ler a entrada dos usuários da tela da console


Para usar o Scanner você declara da seguinte forma: 
``` java
String input = scanner.next();
```

Onde você cria uma variável e ela recebe o Scanner, assim atribuindo o valor digitado pelo usuário.

### Métodos mais uteis do Scanner

|Método | O que ele Faz | Quando usaro|
| -------- | -------- | -------- |
| nextInt() | Semelhante a next(), esta função lê a entrada do usuário e retorna seu valor do inteiro. | Quando você solicita um valor inteiro |
| hasNext()| Retorna verdadeiro, se o scanner tiver outra entrada, caso contrário, falso.| Quando quiser saber se há mais entrada para o scanner ler.|
| close() | Fecha o scanner. | Quando terminar de ler a entrada, é melhor fechar o scanner, principalmente ao ler a entrada da tela da console. Isso mantém o programa em execução continuamente. O scanner pode esperar mais entrada, se nunca foi fechado.|


## Operadores Relacionais 

|Operador | Definição |
| -------- | -------- |
| > | Maior que |
|>= |Maior que ou igual a|
|== |Igual a|
|< |Menor que|
|<= |Menor que ou igual a|
|!= |Não é igual a|

## Operadores Relacionais

| Operador | Definição |
|-----------|-----------|
| && | E |
| \|\| | OU |
| ! | NÃO |


## Sintaxe das estrutras if-else

``` java
if(condição) {
    método
} else if{
    método
} else {
    método
}
```

> Não sendo obrigatório ter else if, ou else, também podendo ter mais de um else if se necessário.

## Loop 

Um loop serve para executar uma ação repetidamente com diferentes entradas. 

Existem três tipos de loops principais, o while-true, do-while e for.

### while-true

Esse loop primeiro verifica a condição e depois executa o código.

```java
while(condition is true){
//logic
}//fim while
```

### so-while

Esse loop primeiro executa o código e depois verifica a condição. 

```java
do{
//statements to repeat go here
} while(condition);
```

### for

Esse loop é recomendado para quando se sabe exatamente quantas vezes ele deve ser executado. 

```java
for(int i=0; i < timesToRun; i++){
//logic
}//fim for
```

#### Break e Continue

Não entendi a aplicabilidade deles em um loop