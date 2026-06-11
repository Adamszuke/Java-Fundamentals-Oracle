# JAVA

## Java JDK e Java JRE
 
| | JRE | JDK |
|-|-----|-----|
| **Função** | Executa programas Java | Desenvolve e executa programas Java |
| **Contém** | JVM + Java API | JRE + ferramentas de desenvolvimento |
| **Quando usar** | Para rodar aplicações | Para programar em Java |
 
**Ferramentas incluídas no JDK:**
 
- `javac` — compilador (transforma `.java` em `.class`)
- `java` — interpretador / executor
- `javadoc` — gerador de documentação
- `jar` — empacotador de aplicações
- `appletviewer` — visualizador de applets *(obsoleto)*
**Componentes do JRE:**
 
- **JVM (Java Virtual Machine)** — lê e executa o bytecode, garantindo que o programa rode em qualquer sistema operacional
- **Java API** — coleções de código pré-escrito para tarefas comuns (texto, rede, interface gráfica)
> É necessário instalar um JRE específico para cada plataforma, pois a JVM embutida nele sabe como lidar com aquele ambiente.
 
**Verificar se o Java está instalado:**
 
```bash
java -version   # Windows ou Linux: no terminal
                # Mac: via Atualização de Software do menu Apple
```
 
---
 
## IDE Java
 
Uma **IDE (Integrated Development Environment)** é o ambiente onde você escreve, compila e executa seu código.
 
A Oracle Academy usa o **Eclipse**, mas os conceitos se aplicam ao VS Code, IntelliJ e outros.
 
### Componentes da IDE
 
| Componente | Função |
|------------|--------|
| **Editor** | Área onde você digita o código-fonte |
| **Views** | Subjanelas com informações do projeto (Package Explorer, Problems, Console) |
| **Perspectiva** | Combinação de views + editor configurada para uma tarefa |
 
### Hierarquia no Eclipse
 
```
Workspace (espaço de trabalho)
 └── Project (projeto — container dos arquivos)
      └── Package (pacote — organiza classes relacionadas)
           └── Classe.java
```
 
> Um **Workspace** é um conjunto de projetos. Um **Project** é como programadores organizam os arquivos Java. Um **Package** garante que arquivos relacionados se encontrem.
 
---
 
## Fluxo para Criar um Programa Java
 
```
1. Criar um Projeto
2. Criar um Pacote (dentro da pasta src/ do projeto)
3. Criar as Classes no pacote
   └── Pelo menos uma deve conter o método main (Classe Driver)
4. Compilar o código → gera arquivo .class (bytecode)
5. Executar a classe Driver
```
 
> No Eclipse, a compilação acontece automaticamente ao salvar. Erros de sintaxe são destacados em tempo real.
 
---
 
## Comentários em Java
 
Comentários são ignorados pelo compilador — servem para documentar o código.
 
```java
// Comentário de uma única linha
 
/* Comentário em bloco
   pode ocupar várias linhas */
 
/**
 * Comentário Javadoc — usado para gerar documentação oficial
 * @param nome descrição do parâmetro
 * @return descrição do retorno
 */
```
 
---
 
## Erros de Sintaxe
 
O IDE destaca erros de sintaxe em tempo real. Os mais comuns:
 
| Erro | Causa |
|------|-------|
| Falta de `;` | Toda instrução termina com ponto e vírgula |
| `{` sem `}` correspondente | Todo bloco aberto precisa ser fechado |
| Nome de classe diferente do arquivo | `public class Student` precisa estar em `Student.java` |
| Tipo errado | Atribuir `String` a um `int`, por exemplo |
 
---
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

## Tipos de dados

Os tipos de dados definem o tipo de dado que uma variável irá armazenar, devendo ser declarado ou inferido e o programa não irá funcionar se o tipo de dado errado foir declarado.

> Tipos de dados incorretos em expressões ou dados são marcados como erros no tempo de compilação.

O java tem oito tipos de dados primitivos.

<table>
    <tr>
        <th>Tipo de dado</th> 
        <th>Descrição do dado</th>
    </tr>
    <tr>
        <td>boolean</td>
        <td>Armazena se um dado é verdadeiro ou falso.</td>
    </tr>
    <tr>
        <td>byte</td>
        <td>Armazena inteiros de -128 a 127.</td>
    </tr>
    <tr>
        <td>char</td>
        <td>Armazena um caractere Unicode de 16 bits de 0 a 65.535</td>
    </tr>
    <tr>
        <td>short</td>
        <td>Armazena inteiros de -32.768 a 32.767.</td>
    </tr>
    <tr>
        <td>int</td>
        <td>Armazena inteiros de: -2.147.483.648 a 2.147.483.647</td>
    </tr>
    <tr>
        <td>long</td>
        <td>Armazena inteiros de: -9.223.372.036.854.775.808 a 9.223.372.036.854.775.807</td>
    </tr>
    <tr>
        <td>float</td>
        <td>Armazena um número decimal positivo ounegativo de: 1.4023x10-45 a 3.4028x10+38</td>
    </tr>
    <tr>
        <td>double</td>
        <td>Armazena um número decimal positivo ou negativo de: 4.9406x10-324 a 1.7977x10+308</td>
    </tr>

</table>

### Declaração de variaveis

Um literal deve ser designado para representar a variavel; 

Um literal pode ser qualquer número, texto ou outra informação que represente um valor.

#### Extrutura

**Tipo** Variavel = _literal_;


``` Java
boolean result = true;
char capitalC = 'C';
byte b = 100;
short s = 10000;
int i = 100000; 
```

### Regras para nomenclatura de variáveis
- Não use uma palavra reservada ou palavra-chave Java
- Não use espaço no nome da variável
- Use uma combinação de letras ou uma combinação de letras e números
- Não é possível começar com um número
- Os únicos símbolos permitidos são o sublinhado ( _ ) e o sinal de dólar ($)

### Convenções para nomenclatura de variáveis
- Use palavras completas em vez de abreviações criptografadas
- Não use variáveis de uma única letra.
- Se todas as variáveis tiverem uma única letra, o código poderá parecer muito confuso
    - Uma exceção a esta convenção é para as variáveis de controle de loop, que são geralmente as letras i, j ou k
- Se um nome de variável consistir em uma palavra, escreva essa palavra com todas as letras minúsculas
- Se um nome de variável consistir em mais de uma palavra, use lowerCamelCase
- Se uma variável for um valor constante, use todas as letras maiúsculas e separe-as com o sublinhado
- Use nomes que expressem a finalidade da variável
- No exemplo a seguir, PI é uma boa escolha para nomear esse número, pois permite que você lembre o que é a variável: 

``` Java
double PI = 3.14159;
```

### Incrementos e decrementos

Incremento significa adicionar um e decremento significa remover um;

São simbolizados como ++ e --;

#### Notação pré-incremento: 

> ++x 

``` java
int x = 3;
++x; //x é igual a 4
z = ++x; //x é igual 4, então z é igual a 5
```
#### Notação pós-incremento:

> x++ 

``` java
int x = 3;
x++; //x is equal to 4
z = x++; //z is equal to 4, THEN x is equal to 5
```


### Truncamento e divisão por número inteiro

A divisão de dois números inteiros sempre irá gerar um número inteiro, por exemplo: 
> Se dividir 1/3 ele será avaliado como 0 em java devido a divisão de inteiros. 

Para calcular um quociente sem truncamento, converta o dividendo para decimal.

> 11 / 5,0 = 2,2 e, do mesmo modo, 11,0 / 5 = 2,2

### Tipos e conversões 

Existem formas de impor uma fórmula para não truncar o valor. (O java não faz isso automaticamente)

> Colocando a fórmula uma fração no fim da conta para que transforme um integer em um double.

```java
double volume = 3.14 * radius * radius * height * 1 / 3;
```

> Transforme um dos integers de literais em um double de
literal de modo que o Java sempre use um double e um
integer e converta implicitamente a resposta em um double,
não truncado.

```java
double volume = 1 / 3.0 * 3.14 * radius * radius * height;
```
> Não entendi essa segunda forma.

#### Usando Casting de tipo 

Usando o casting de tipo você adiciona o tipo antes do valor entre parenteses.

```java
int number;
number = (int)(Math.random() * 10);
System.out.println("The random number is " + number + ".");
```

> Algumas alterações não serão possíveis, como por exemplo de converter uma char em uma string.


Quando é feita uma transição de um tipo primitivo menor para um tipo primitivo maior a transição é feita implicitamente, e quando é feito de um tipo primitivo maior para um menor deve ser feito de forma explícita.

> byte → short → int → long → float → double
>
> (menor)→(maior)

### Casting Implícito vs Explícito

Quando você vai de um tipo que "cabe menos" para um que "cabe mais", o Java faz sozinho — não tem risco de perder informação. Quando é o caminho contrário, você precisa avisar explicitamente que aceita o risco.






### Notas 

> camelCase é a prática de sequenciarPalavrasCapitalizadas juntas sem espaços. Letras minúsculas concatenadas não capitalizam a palavra principal.

> Applets Java eram pequenos programas escritos na linguagem Java, embutidos diretamente em páginas da web e executados dentro do navegador do usuário, utilizando a Máquina Virtual Java (JVM)

> Um objeto em Java é uma instância concreta de uma classe. Ele representa um elemento do mundo real (como um "carro" ou "conta bancária") ou um conceito abstrato no código, possuindo atributos (dados/características) e métodos (comportamentos/ações) definidos por seu molde.

> Truncamento é o conceito de remover a parte fracionária ou decimal de um
número. Por exemplo: O truncamento de 7,8 produzirá o resultado 7, e o
truncamento de -3,2 produzirá o resultado -3.


## Fontes

[Slide JF4-1-1](../slides/JF4-1/JF4-1-1.pdf)

[JDK, JRE, JVM e JIT](https://blog.grancursosonline.com.br/jdk-jre-jvm-e-jit/)
