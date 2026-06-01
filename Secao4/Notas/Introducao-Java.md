# JAVA

## Java JDK e Java JRE

- O <b>Java Development Kit (JDK)</b> é o conjunto de ferramentas necessárias para realizar o desenvolvimento de aplicações Java. Contendo: 

    - Java Runtime Environment (JRE); e Ferramentas de programação:
    - javac: compilador;
    - java: interpretador;
    - appletviewer: visualizador de applets;
    - javadoc: gerador de documentação;
    - jar: empacotador de aplicações.

- O <b>Java Runtime Environment (JRE)</b> é um pacote de software que fornece os requisitos mínimos para executar programas ou aplicativos desenvolvidos na linguagem Java. 

    - <b>JVM (Java Virtual Machine)</b>: A Máquina Virtual Java. É o "coração" do JRE, responsável por ler e executar o código compilado em Java (bytecode), garantindo que o programa rode em qualquer sistema operacional.
    - <b>Java Application Programming Interface (Java API)</b>: Coleções de códigos pré-escritos que os programas Java podem usar para realizar tarefas comuns (como manipulação de texto, rede ou interface gráfica).

```
É necessário instalar um JRE específico de uma plataforma, pois junto com ele vem uma JVM que saberá lidar com essa plataforma e conseguirá executar aplicações Java naquele ambiente.
```

### Classe 

Uma classe em Java é um modelo que armazena atributos (características) e métodos (comportamentos). 

```` Java
public class Carro {
    // 1. Atributos (Características)
    String modelo;
    int ano;
    
    // 2. Construtor (Inicializa os atributos ao criar o objeto)
    public Carro(String modelo, int ano) {
        this.modelo = modelo;
        this.ano = ano;
    }
    
    // 3. Métodos (Comportamentos)
    public void acelerar() {
        System.out.println("O " + modelo + " está acelerando!");
    }
}
````

- <b>Atributos</b>: Variáveis que guardam o estado ou dado do objeto.
- <b>Construtor</b>: Cria um objeto com dados iniciais. 
- <b>Métodos</b>: Função que determina o que o objeto pode fazer e como ele lida com dados.
- <b>Modificadores de Acesso</b>: "public, private e protected", define quem pode alterar e visualizar os dados do objeto.



### Método main

O método main é o método principal na sua aplicação Java, é apartir dele que a JVM começa a ler e executar o programa. 

````Java
public class Principal {
    // psvm = Atalho para gerar essa linha
    public static void main(String[] args) {
        // Seu código começa a executar aqui
        System.out.println("Olá, mundo!");
        // sout = atalho para gerar a linha de cima
    }
}
````


## Formato geral do programa Java

Há dois formatos de classe Java
 - Classes Driver
 - Classes de Objeto


### Classes Driver

Contêm o método main.

É necessário um método main para executar um programa Java.

O método main pode conter: 
- Intância de objetos de classes objeto;
- Variáveis;
- Loops, Condicionais (if-else);
- Outros métodos;
- Outra lógica de programação;


### Classes de Objeto

São classes que definem os objetos que podem ser usados na classe driver. 


### Termos chave

<table>
<tr>
    <th>Termo</th>
    <th>Definição </th> 
</tr>

<tr>
    <td>package</td>
    <td>
•  Define a localização desta classe em relação a outras classes, e fornece um nível de controle de acesso.

• Use modificadores de acesso (como public e private) para controlar o acesso.
    </td>
</tr>

<tr>
    <td>import</td>
    <td>
• Define outras classes ou grupos que você está usando em sua classe.

• A instrução de importação fornece as informações do compilador que identificam as classes externas usadas na classe atual.
    </td>
</tr>

<tr>
    <td>class</td>
    <td>
• Precede o nome da classe.

• O nome da classe e o nome do arquivo devem coincidir quando a classe for declarada como pública (o que é uma boa prática).

• No entanto, a palavra-chave public na frente da palavra-chave class é um modificador e não é necessária.
    </td>
</tr>

<tr>
    <td>variáveis de classe</td>
    <td>
• Variáveis ou os dados associados a programas (como
integers, strings, arrays e referências a outros objetos).
    </td>
</tr>


<tr>
    <td>Métodos</td>
    <td>
• Os métodos podem ser executados em um objeto
• Eles também são chamados de métodos de instância
• Os métodos podem retornar valores da variável de
objeto (às vezes chamada de funções) ou podem alterar
os valores da variável de um objeto.
    </td>
</tr>

<tr>
    <td>Construtores</td>
    <td>
• Métodos chamados durante a criação (instanciação) de
um objeto (uma representação na memória de uma
classe Java.)
    </td>
</tr>

</table>


## Palavras-chave Java
 
Palavras reservadas com função especial na linguagem — **não podem** ser usadas como nomes de classes, métodos ou variáveis.
 
Exemplos: `class`, `public`, `private`, `int`, `double`, `String`, `for`, `while`, `if`, `new`, `return`, `this`, `final`, `import`, `package`, `void`, `static`
 
> No IDE Java, palavras-chave aparecem em uma cor diferente automaticamente.

## Palavra-chave `package`
 
Agrupa classes e fornece um namespace (como uma pasta no sistema de arquivos).
 
```java
package com.example.domain;
```
 
Recomenda-se sempre declarar o pacote no topo da classe.
 
**Exemplo de estrutura:**
```
+com
 |_+acme
    |_+jones
       |_+Student.java
       |_+Teacher.java
```
Namespace: `com.acme.jones.Student`

## Palavra-chave `import`
 
Identifica pacotes ou classes externas que você quer usar na sua classe.
 
```java
import java.util.Scanner;       // importa uma classe específica
import java.util.*;             // importa o pacote inteiro
import java.util.Date;          // múltiplas importações
import java.util.Calendar;
```
 
> Toda classe importa `java.lang` automaticamente. Não é necessário importar classes do mesmo pacote.
 
---
 
## Criando uma Classe de Objeto: `Student`
 
### Variáveis de classe
 
```java
package com.example.domain;
 
public class Student {
    private int studentId;          // lowerCamelCase, private
    private String name;
    private String ssn;
    private double gpa;
    public final int SCHCODE = 34958; // constante: UPPER_SNAKE_CASE, public
```
 
> Variáveis de classe devem ser `private` para proteger os dados (encapsulamento).  
> Constantes são declaradas com `public final` e em letras maiúsculas.
 
---
 
## Construtores
 
Um construtor é um método especial que **cria uma instância da classe**.
 
Características:
- Mesmo nome da classe
- Não declara tipo de retorno
- Invocado com a palavra-chave `new`
### Construtor padrão (sem parâmetros)
 
```java
public Student() {
    studentId = 0;
    name = "";
    ssn = "";
    gpa = 0.0;
} // fim do construtor
```
 
> Se nenhum construtor for declarado, o Java fornece um construtor padrão em branco automaticamente. Se você declarar pelo menos um construtor, o padrão automático deixa de existir.
 
### Construtor com parâmetros
 
```java
public Student(int x, String n, String s, double g) {
    studentId = x;
    name = n;
    ssn = s;
    gpa = g;
} // fim do construtor
```


### Notas 
```
camelCase é a prática de sequenciarPalavrasCapitalizadas juntas sem
espaços. Letras minúsculas concatenadas não capitalizam a palavra principal.
```
```
Applets Java eram pequenos programas escritos na linguagem Java, embutidos diretamente em páginas da web e executados dentro do navegador do usuário, utilizando a Máquina Virtual Java (JVM)
```

```
Um objeto em Java é uma instância concreta de uma classe. Ele representa um elemento do mundo real (como um "carro" ou "conta bancária") ou um conceito abstrato no código, possuindo atributos (dados/características) e métodos (comportamentos/ações) definidos por seu molde.
```

<b></b>


## Fontes

[Slide JF4-1-1](../slides/JF4-1/JF4-1-1.pdf)

[JDK, JRE, JVM e JIT](https://blog.grancursosonline.com.br/jdk-jre-jvm-e-jit/)
