# Threads

Permite que um processo realize diversas tarefas de forma concorrente.

* Por estarem dentro de um mesmo processo, compartilhando variáveis, a comunicação entre threads tende a ser mais eficiente e mais fácil de ser feita do que a comunicação entre dois processos distintos

```java
public class Fluxo1 extends Thread{
    public void run(){
        for(int i=0; i<10;i++){
        //...
        }
    }
}
``` 

```java
public class Fluxo2 implements Runnable{
    public void run(){
        for(int i=0; i<10;i++){
            //...
        }
    }
}
``` 

```java
public class Fluxo3 extends Thread{
    public Fluxo3(String nome){
        super(nome);
    }

    public void run(){
        try{

            System.err.println( this.getName() + " vair dormir...");
            Thread.sleep(1000);

        } catch(InterruptedException e){
            System.err.println(e.toString());
        }
        System.err.println(this.getName() + " acordou...");
    }
}
``` 