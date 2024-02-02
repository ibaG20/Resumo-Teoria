# Tratamento de Exceções
  - Com o tratamento de exceções é possível capturar e tratar os erros do código e criar um programa tolerante a falhas
  - É muito importante para a confiabilidade do Software
  
## Exceções
  - *Definição*: corresponde a um evento que ocorre durante a excecução de um programa e interrompe o fluxo de código
  - *Tipos de exceção*:
   
    * *Checked*: verificadas em tempo de compilação
    * *Unchecked*: não verificadas em tempo de compilação

## Blocos Try-Catch
  - *Definição*: o bloco **try** contém o código que pode gerar uma exceção, e o bloco **catch** contém o código que trata a exceção
  - *Exemplo*: 
~~~java
try {
    // Código que pode gerar uma exceção
} catch (TipoDeExcecao e) {
    // Código para tratar a exceção
}
~~~

## Multiplos Blocos Catch
  - *Definição*: é possível ter multiplos blocos **catch** para lidar com diferentes tipos de exceções
  - *Exemplo*:
~~~java
try {
    // Código que pode gerar uma exceção
} catch (TipoDeExcecao1 e) {
    // Tratamento para TipoDeExcecao1
} catch (TipoDeExcecao2 e) {
    // Tratamento para TipoDeExcecao2
}
~~~

## Bloco Finally
  - *Definição*: é um bloco opcional, e é executado sempre, independente de ocorrer ou não uma exceção
  - *Exemplo*:
~~~java
try {
    // Código que pode gerar uma exceção
} catch (TipoDeExcecao e) {
    // Tratamento para a exceção
} finally {
    // Código que será executado sempre
}
~~~

## Exceções Verificadas e Não Verificadas
  - As exceções verificadas são aquelas no qual é obrigatório tratar, e as não verificadas são opcionais.
  - *Verificadas*: 
     - Usadas para erros recuperáveis (ele pode ser tratado).
     - Caso algum valor esteja errado e seja preciso corrigir para o funcionamento correto do programa.
     - Herdam de Exception. 
     - São forçadas pelo compilador e usadas para indicar condições excepcionais, que estão fora do controle do programa.
  - *Não verificadas*: 
     - Usadas para erros irrecuperáveis.
     - Caso surja um NullPointerException inesperado na aplicação, ele não pode ser tratado. Só é possível mostrar uma mensagem amigável ao usuário.
     - Herdam de RuntimeException. 
     - Ocorrem durante o tempo de excecução e são usadas para indicar erros.

## Lançamento de Exceções
  - *Throw*: Usado para lançar uma exceção explicitamente
  - *Throws*: Usado na declaração de método para indicar que um método pode lançar uma exceção
  - *Exemplo*:
~~~java
void meuMetodo() throws MinhaExcecao {
    // Código que pode lançar MinhaExcecao
}
~~~

## Criação de Exceções Personalizadas
  - *Definição*: é possível desenvolver classes de exceções personalizadas pra situações específicas
  - *Exemplo*:
~~~java
public class MinhaExcecao extends Exception {
    // Implementação da exceção personalizada
}
~~~

## Try-With-Resources (Java 7+)
  - *Definição*: Recurso criado para automatizar o fechamento de recursos, tais como arquivos, conxões, dentre outros.
  - *Exemplo*:
~~~java
try (Recurso recurso = new Recurso()) {
    // Código que utiliza o recurso
} catch (TipoDeExcecao e) {
    // Tratamento da exceção
}
~~~

## Suppressed Exceptions (Java 7+)
  - *Definição*: Permite que seja adicionada uma exceção secundária a uma exceção principal
  - *Exemplo*:
~~~java
try {
    // Código que pode gerar exceções
} catch (ExceptionPrincipal | ExcecaoSecundaria e) {
    // Tratamento de exceções
    Throwable excecaoSecundaria = e.getSuppressed()[0];
}
~~~

## Método "getMessage()" e "printStackTrace()"
  - *getMessage()*: Retorna a mensagem associada a exceção
  - *printStackTrace()*: Exibe a pilha de chamadas do ponto onde a exceção ocorreu.