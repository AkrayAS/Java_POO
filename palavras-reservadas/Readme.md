# Palavras Reservadas

### Palavra Reservada: this

this é uma referência para o próprio objeto e pode ser usado para garantir que estará referenciando os membros de uma classe e não uma variável local

### Membros não estáticos

* Atributos não estáticos - Cada instância da classe terá uma cópia distinta desse atributo.

* Método estático não pode acessar membros não estáticos.


```java
public class Celular {
    private static int total = 0;
    private int creditos = 0;

    public Celular(int creditos){
        total++; this.creditos = creditos;
    }
    // OK
    public int getCreditos() { 
        return creditos;
    }
    // OK
    public int getTotal(){ 
        return total; 
    }
    // ERRO DE SINTAXE
    public static int retornaCreditos(){
        return creditos;
    } 
 }
```

### Modificador final

Pode ser usado em atributos, métodos ou em variáveis locais. Uma variável após ter recebido um valor, esse não poderá ser alterado, métodos não poderão ser sobrescritos (conceito de herança)

```java
public class Celular{
    private final String FREQUENCIA = "1800";
    private final int SERIAL;

    public Celular(int s) {
        this.SERIAL = s;
    }

    public final void iniciarChamada(){
        //...
    }
}
```

### Classes utilitárias

* java.lang.Math

* StringBuilder