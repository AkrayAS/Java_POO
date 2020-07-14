# Tratamento de exceções e Coleções

### Tratamento de exceções

* Exceção - Evento que indica a ocorrência de algum problema durante a execução do programa

O tratamento de exceçôes permite aos programas capturar e tratar erros em vez de deixá-los ocorrer e assim sofrer com as consequências. (Utilizado em situações em que o sistema pode recuperar-se do mau funcionamento que causou a exceção)

```java
public int lerTeclado(){
 Scanner teclado = new Scanner(System.in);
 do{
    try{
        System.out.print("Entre com um n´umero: ");
        int num = teclado.nextInt();
        return num;
    } catch(Exception e) {
        System.err.println("Erro: " + e.toString());
    }finally{
        System.out.print("Sempre ser´a executada");
    }
    System.out.print("Se o return for executado, ent~ao essa linha naoser´a");
    }while(true) {
     //...
    }
}
```

### Coleções

Em java coleção é um objeto que agrupa múltiplos elementos dentro de uma única unidade(Usadas para armazenar, obter e manipular dados agregados). O java Collections Framework provê também algoritmos para busca e ordenação em coleções.

### Java Collections Framework

* Set - Coleção que não permite elementos duplicados

* List - Coleção ordenada de elementos e permite elementos duplicados

* Queue - Fila que ordena elementos para serem processados posteriormente, por exemplo, FIFO

* Map - Mapeia chaves para valores. Não permite chaves duplicadas e cada chave pode mapear somente um valor