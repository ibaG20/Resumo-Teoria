# Orientação a Objetos
  - É um paradigma de programação que se baseia na organização de objetos interconectados.
  
## Objetos
  - *Definição*: Um objeto é uma instância concreta de uma classe, representando entidades
  - *Exemplo*: Carro meuCarro = new Carro();

## Classes
  - *Definição*: Uma classe corresponde a um modelo para criar objetos. Ela define atributos (dados) e métodos (comportamentos)
  - *Exemplo*:
  - 
~~~java
  public class Carro {
    String modelo;
    int ano;
    void acelerar() {
        // Implementação do método acelerar
    }
} 
~~~

## Atributos e Métodos
  - *Atributos*: variáveis dentro de uma classe que representam as características do objeto
  - *Métodos*: funcções associadas a uma classe que definem comportamentos do objeto
  
## Encapsulamento
  - *Definição*: esconder/proteger detalhes internos de uma classe, e expor apenas o necessário
  - *Exemplo*:
  
    * uso de modificadores de acesso:
  
                + public
                + private
                + protected

## Herança
  - *Definição*: mecanismo que permite uma classe herdar atributos e métodos de outra classe
  - *Exemplo*:
  
~~~java
public class CarroEsportivo extends Carro {
    // Novos atributos e métodos específicos de CarroEsportivo
}
~~~

## Polimorfismo
  - *Definição*: é quando duas classes, ou mais, derivadas de uma mesma superclasse, podem invocar métodos com a mesma identificação, mas com comportamentos distintos especializados para cada classe derivada 
  - *Exemplo*:
~~~java
public interface Veiculo {
    void mover();
}
public class Carro implements Veiculo {
    void mover() {
        // Implementação do movimento de um carro
    }
}

~~~

## Abstração 
  - *Definição*: ocultar detalhes irrelevantes ou completos de um problema e focar no que é essencial para o programa
  - *Exemplo*: definição de classes abstratas e interfaces

## Interface
  - *Definição*: contrato que especifica métodos que uma classe deve imlementar
  - *Exemplo*:
~~~java
public interface Animal {
    void emitirSom();
}
public class Cachorro implements Animal {
    void emitirSom() {
        // Implementação do som de um cachorro
    }
}
~~~

## Contrutores
  - *Definição*: Métodos especiais chamados durante a criação de um objeto através do operador new
  - *Exemplo*:

## Métodos Estáticos e Variáveis de Classe
  - *Definição*: Os métodos estáticos não dependem de um objeto e são cahamados sem que haja uma instancia da classe. Como os métodos estáticos não possuem ligação com um objeto, ele não pode usar variáveis de instancia (variáveis de um objeto)
  - *Exemplo*:
~~~java
public class Util {
    static int somar(int a, int b) {
        return a + b;
    }
}
~~~

## Sobrecarga e Sobrescrita de Métodos
  - *Sobrecarga*: ter multiplas versões de um método com diferentes parametros
  - *Sobrescrita*: implementar um metodo em uma subclasse que ja esta presente na superclasse
  
## Palavra-chave "super"
  - *Definição*: usada pra acessar membros da classe pai
  - *Exemplo*:
~~~java
public class CarroEsportivo extends Carro {
    void acelerar() {
        super.acelerar();
        // Implementação adicional específica de CarroEsportivo
    }
}
~~~