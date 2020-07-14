# Teste de unidade e JavaDOC

### JavaDOC

Gerador de documentação automática com base em comentários escritos no próprio código fonte.

```java
/**
* Classe que realiza a subtração de inteiros
*
* @author Exemplo
*/
public class SubtracaoInteiros {
 
    /**
    * Faz a subtração de dois inteiros
    * @param a operando 1
    * @param b operando 2
    * @return resultado da subtração dos operandos
    */
    public int subtracao(int a, int b){
    return (a-b);
    }
}
```
### Teste de unidade

Processo que visa testar individualmente módulo, componentes ou procedimentos (métodos) de um programa, comparando o funcionamento de um módulo com sua especificação. Possibilita ver se a implementação de um módulo contradiz sua especificação.

> Dependências externas (bibliotecas) devem ser removidas do teste, usando por exemplo, componentes de testes que simulam tais bibliotecas

```java
    assertEquals();
    assertArrayEquals();
    assertFalse("failure - should be false", false);
    assertTrue("failure - should be true", true);
    assertNotNull("should not be null", new Object());
    assertNull("should be null", null);
```