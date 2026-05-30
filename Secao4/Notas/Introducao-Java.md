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


### Notas 
```
camelCase é a prática de sequenciarPalavrasCapitalizadas juntas sem
espaços. Letras minúsculas concatenadas não capitalizam a palavra principal.
```
```
Applets Java eram pequenos programas escritos na linguagem Java, embutidos diretamente em páginas da web e executados dentro do navegador do usuário, utilizando a Máquina Virtual Java (JVM)
```

<b></b>


## Fontes

[Slide JF4-1-1](../slides/JF4-1-1.pdf)

[JDK, JRE, JVM e JIT](https://blog.grancursosonline.com.br/jdk-jre-jvm-e-jit/)
