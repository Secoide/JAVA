# JAVA
 ☕ Detalhes e fundamentos resumidos sobre linguagem JAVA.

## Modificadores de acesso
- **private**: So pode ser acessado na propria classe;
- **protected** : So pode ser acessado no mesmo pacote ou em subclasses de pacotes diferentes;
- **public**: Por ser acessado por todas classes;
- **(nada)**: So pode ser acessado nas classes do mesmo pacote.

## Membros estáticos

- **static:** Não precisa instanciar objeto.

Exemplo: 
```java
Classe calc = new Classe(); //Sem static
Classe.Calcular();  //Com static
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
