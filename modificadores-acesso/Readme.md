# Modificadores de Acesso e Método Construtor

## Classes e Objetos

Um objeto, onde suas características são seus atributos (dados atrelados ao objeto) e seus comportamentos são ações ou métodos. Quando um objeto pode ser classificado, seu objeto pertence à uma classe.

## Encapsulamento

Emissor da mensagem não precisa saber como o resultado foi obtido, para este só importa o resultado. O emissor tambêm precisa conhecer quais operações o receptor sabe realizar ou quais informações o receptor pode fornecer.

### Modificadores de acesso

Indicam quais atributos e métodos de um objeto estarão visíveis aos demais objetos do sistema.

* private - Os membros de uma classe (atributos e métodos) definidos como privados só poderão ser acessados pelos demais métodos da própria classe

* public -  – Os membros de uma classe definidos como públicos poderão ser invocados por métodos de qualquer classe

### Sobrecarga de métodos

Uma classe pode ter mais método com o mesmo nome, pórem com assinaturas diferentes.
(Ex: Tipo de retorno, Nome do método, Lista de parâmetros.)

### Método construtor padrão

Método cuja de lista de parâmetros está vazia. Toda classe Java possui um construtor padrão vazia implícito.

* Uma classe pode conter métodos construtores sobrecarregados.

* Ao instanciar um objeto o desenvolvedor indica qual construtor irá chamar.

### Exemplo Ideal

```java
public class Carro {
    //atributos
    private int velocidade = 0;
    
    //método construtor padrão
    public Carro() {}

    //método construtor sobrecarregado
    public Carro(int v) {
        this.velocidade = v;
    }

    //metodos
    public void acelerar(int v){
    //...    
    }

    public void frear(int v){
    //...
    }
}
```