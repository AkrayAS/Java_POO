# Classe abstrata, interfaces e Polimorfismo

### Classe Abstrata

* Não é possível instanciar objetos de uma classe abstrata

* Pode conter métodos concretos e métodos abstratos 

* Todo método abstrato deve ser obrigatoriamente sobrescrito pelas subclasses, métodos concretos não precisam ser sobrescritos

* Uma subclasse que não prover implementações para os métodos abstratos herdados, deve obrigatoriamente ser abstrata

```java
public abstract class FormaGeometrica{
    public abstract void desenhar();
}

public class Ponto extends FormaGeometrica{
    private int x;
    private int y;

    @override
    public void desenhar() {
        //...
    }
}
```

### Interface

* O conceito de herança múltipla pode ser obtido em Java fazendo uso de Interfaces

* herança múltipla de tipos – uma classe pode implementar mais de uma interface

* herança múltipla de implementação – habilidade de herdar as definições de métodos de múltiplas interfaces

Uma Interface é Java é semelhante a uma classe abstrata, porém só pode conter constantes, métodos abstratos e métodos default

```java
public interface Carro {
    public static final String nome = "Carro";
    
    void frear(int intensidade);
    
    default void desligar() {
        //...
    }
}

public class Fusca implements Carro {
    public void frear(int intensidade){
        //...
    }
}
```

### Polimorfismo

Permite desenvolver sistemas que sejam facilmente extensíveis de forma que novas classes possam ser adicionadas ao sistema exigindo pouca ou nenhuma modificação nas partes gerais do sistema