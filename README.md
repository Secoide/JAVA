# JAVA
 ☕ Detalhes e fundamentos resumidos sobre linguagem JAVA.

## Classes

### Herança ⬅️
Associação que permite uma subclasse herde todos os dados de uma outra classe.
- **extends**: Extende todos os atributos e metodos da classe mãe.
```java
public class ClasseFilho extends ClasseMae
```
### Modificadores de acesso 📦
- **private**: Só pode ser acessado na própria classe;
- **protected** : Só pode ser acessado no mesmo pacote ou em subclasses de pacotes diferentes;
- **public**: Por ser acessado por todas classes;
- **(nada)**: Só pode ser acessado nas classes do mesmo pacote. 

 


### Membros Estaticos, Métodos
- **static:** Não precisa instanciar objeto.
Exemplo: 
```java
Classe calc = new Classe(); //Sem static
Classe.Calcular();  //Com static
```
- **abstract**: Não deixa instanciar uma classe.
```java
public abstract class Teste()

public static void main(){
 Teste tt = new Teste();      //Não sera possivel instanciiar
}
```
>Atenção: Se um metodo é abstrato a classe obrigatoriamente devera ser abstrata também.
>Os métodos abstratos não possuem implementação.
- **super**: Chama a implementação de um superclasse na subclasse.
- **final**: evita que a classe seja herdada e o metodo nao seja sobreposto
```java
public final class Exemplo
public class Subexemplo extends Exemplo //Erro: não é possivel extender classe com final


public final void Teste() //qualquer outra subClasse extendida, não poderá sobrepor este metodo.
```


## Enumerações
- **enum**
>Um tipo de enum é um tipo de dados especial que permite que uma variável seja um conjunto de constantes predefinidas
```java
public enum Dia {
    SEGUNDA, TERÇA, QUARTA, QUINTA, SEXTA, SABADO, DOMINGO 
}
```

## Anotações
São avisos antecipados para o compilador.
- **@Override**:


## Polimorfismo

### Upcasting
Converte um objeto da subclasse para superclasse.
```java
Exemplo exe = New SubExemplo();
```

### Downcasting
Converte um objeto da superclasse para subclasse.
```java
SubExemplo sub = (SubExemplo) exe;
```
>Atenção: Devido o compilador nao reconhecer qual subclaase a superclasse recebeu upcasting, devemos realizar a verficação manualmente. Logo devemos usar o instanceof.
- **instanceof**: Verifica se um objeto é um tipo especifico de classe;
```java
if (exe instanceof SubExemplo){
    SubExemplo sub = (SubExemplo) exe;
]
```


## Comportamento da Memória
### Boxing 
Processo de conversão de um objeto tipo valor para um objeto tipo referência compatível;
```java
int x = 20;  //Stack
Object obj = x; //Aponta para o Heap
```
_Lembrando: Stack e Heap são formas de organização de dados na memória._
### Unboxing 
Processo de conversão de um objeto tipo referência para um objeto tipo valor compatível;
```java
int x = 3;
Object obj = x; 
int y = (int) obj; //Cast
```
>Necessario realizar um [Cast]("") para não acusar erro;

### Wrapper classes 
São Classes com objetivo de nao se precupar com Conversões e utlizações de Cast ;
```java
int x = 3;
Object obj = x; 
int y = (int) obj; //Cast
```
_Ressalva-se: Wrapper aceitam valores nulos._


### Basico
> Estruturas usuais, comum em muito linguagem, mudandado apenas alguns detalhes.

#### Laços 🔄

- **for each**: sintaxe mais simplificada para percorrer coleções.
```java
for (String obj : vetor){
   sysout(obj);
}
```
