# Dúvidas

Não entendi a diferença de criar um Java Project e um Java Package, também não entendi porque a certificação fica pedindo para criar uma versão com Package e a outra sem. 

````
São coisas em níveis diferentes — não concorrentes.
Um Java Project é o container total: a pasta raiz com todo o código, bibliotecas (lib/), fontes (src/), configurações. É o que você cria uma vez no VS Code ou IntelliJ.
Um Java Package é um namespace dentro do projeto para organizar as classes. Funciona como pastas lógicas que evitam conflito de nomes e agrupam classes relacionadas. Você declara no topo do arquivo:
javapackage com.oracle.exemplos;   // ← isso é o package

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello");
    }
}
Quando tem package, o arquivo precisa estar no caminho de pasta correspondente: src/com/oracle/exemplos/HelloWorld.java. Quando não tem, a classe fica no "default package" — direto em src/HelloWorld.java, como você já está fazendo.
A certificação pede os dois porque quer que você saiba que o default package existe (e é válido para exemplos simples), mas que em projetos reais sempre se usa package. Isso cai em questão diretamente.

````

Explicação do Claude