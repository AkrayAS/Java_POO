# Herança

Uma classe herda atributos e métodos de uma outra classe. 

> Ideal para casos onde são necessárias classes distintas para atacar
problemas específicos. Porém, tais classes necessitam compartilhar um
núcleo comum

```java
public class Telefone{
 public void ola(){
    System.out.println("Ola, sou um telefone");
 }
}
public class Semfio extends Telefone{
    public void ola(){
        System.out.println("Ola, sou um telefone sem fio");
    }
}
 public class Principal{
    public static void main(String args[]){
        Telefone t = new Telefone();
        Semfio s = new Semfio();
        t.ola(); // Ola, sou um telefone
        s.ola(); // Ola, sou um telefone sem fio
    }
 }
```