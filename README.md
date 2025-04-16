# Exercício Zoológico - Polimorfismo

Este exercício é uma continuação do exercício anterior do Zoológico, no qual havíamos trabalhado o conceito de herança.

Nosso objetivo será entender melhor os **conceitos relacionados ao polimorfismo** e melhorar a modelagem de nossas classes, percebendo como eles nos ajudam a **evitar duplicação** de código nas classes que **utilizam** classes de uma hierarquia de herança.

## Orientações Gerais

- Você deve fazer um passo de cada vez, testá-lo, fazer o commit e enviar suas alterações.
Somente depois disso é que você deve passar para o próximo passo.

- **ATENÇÃO**: **desligue o GitHub Copilot para fazer o exercício!**
  - Se você utilizá-lo você não estará realmente exercitando os conceitos aprendidos e
    não terá o domínio adequado para desenvolver as habilidades necessárias para se tornar
	um bom programador/desenvolvedor.
  - Sem contar ainda a questão do plágio.
  - Lembre-se que você pode (e deve) consultar os materiais da disciplina para fazer o exercício.

- Esse arquivo README pode ser melhor visualizado no VS Code (com formatação adequada) 
  abrindo-o no modo de visualização. Para isso, basta apertar Ctrl+Sfhit+V com ele aberto.


## Passo 0 - Continuando a partir do exercício anterior

Baixe o repositório do exercício anterior do Zoológico, e copie os arquivos `.java` da pasta `src` para a pasta `src` deste projeto.

Execute o programa e teste para confirmar que não ficou faltando nenhum arquivo.

Faça um commit com essas alterações, usando a mensagem: "Passo 0" e sincronize suas alterações.

## Passo 1 - Experimentando Polimorfismo

Vamos começar exercitando nosso entendimento sobre os conceitos de polimorfismo.
Para isso, crie uma classe chamada `Teste` com um método `main` e, dentro dele, faça o seguinte:

- Declare uma variável chamada `animal` do tipo `Animal` e atribua a ela um objeto da classe `Elefante`.
- Chame o método `getNome` usando a variável `animal`.
- Agora, usando a mesma variável `animal`, atribua a ela um objeto da classe `Gavião`.
- Chame o método `getNome` usando a variável criada.

Explique abaixo, da forma mais completa possível, como é possível que a mesma variável `animal` possa ser usada para chamar métodos de objetos de classes diferentes.

>  ... escreva aqui a sua resposta ...

Ao terminar, faça um commit com as alterações da classe `Teste` e as alterações neste arquivo README.

## Passo 2 - Experimentando Polimorfismo 2

Agora, altere a classe `Teste` fazendo o seguinte:
- Crie um método chamado `metodoTeste` que recebe uma parâmetro do tipo `Animal`.
  - Dentro dele, chame o método de descrição completa usando o objeto recebido por parâmetro.
  - E exiba o resultado na tela.
- No método `main`, chame o método `metodoTeste` passando um objeto da classe `Elefante`.

O que é exibido?

>  ... escreva aqui a sua resposta ...

O método de descrição completa chamado inicialmente pertence a qual classe?

>  ... escreva aqui a sua resposta ...

Agora chame o método `metodoTeste` passando um objeto da classe `Gavião`.

O que é exibido?

>  ... escreva aqui a sua resposta ...

O método de descrição completa chamado inicialmente pertence a qual classe?

>  ... escreva aqui a sua resposta ...

Explique, da forma mais completa possível, como o mesmo trecho de código (método `metodoTeste`) pode ser usado para chamar métodos de classes diferentes.

>  ... escreva aqui a sua resposta ...

Ao terminar, faça um novo commit com as alterações (na classe Teste e neste arquivo README).
E não se esqueça de sincronizar suas alterações.

## Passo 3 - Aplicando Polimorfismo no Projeto Zoologico

Vamos agora perceber como o polimorfismo ajuda a reduzir a replicação de código nas classes que utilizam classes de uma hierarquia de herança. 

Para isso, você deve alterar a classe `Zoologico`:

- Substitua as coleções de animais de cada espécie por uma única coleção (`HashMap`) com todos os animais.
- E, devido a essa modificação, implemente as alterações necessárias nos métodos da classe.

Do ponto de vista do usuário, seu programa deverá continuar funcionando da mesma forma que você havia feito no exercício da aula anterior.
Mas repare que agora seu projeto terá um *Design* de classes melhor.

Teste suas alterações!

Ao final, faça um novo commit no seu repositório.

## Passo 4 - Herança, Polimorfismo e Evolução do Sistema

Suponha que nosso Zoológico recebeu animais de uma nova espécie: peixe-boi.

Faça todas as alterações necessárias no sistema para que o Zoológico possa agora ter animais da espécie peixe-boi. 
Em seguida, responda às perguntas abaixo.

Se a espécie peixe-boi fosse tratada no exercício da semana passada, o que você implementaria do mesmo jeito e o que teria que ser implementado de forma diferente?

>  ... escreva aqui a sua resposta ...

O que a sua resposta anterior tem a ver com as vantagens do polimorfismo?

>  ... escreva aqui a sua resposta ...

## Passo 5 - Identificando o uso de Polimorfismo

Para todas as perguntas abaixo, você deve acrescentar comentários no seu código indicando onde os conceitos são usados, e explicando os conceitos.

a) Acrescente um comentário no seu código indicando uma **variável** que seja **polimórfica** e explique, no próprio comentário, porque ela é uma variável polimórfica.

Exemplo de comentário:

```java
  // Passo 5 (a). A variável xxxx abaixo é polimórfica porque ...
```

b) Acrescente um comentário no seu código indicando onde está sendo usado o **princípio da substituição** e explique o que é este princípio.

Exemplo de comentário:

```java
  // Passo 5 (b). A linha abaixo demonstra o uso do princípio da substituição que é ...
```


c) Acrescente um comentário no seu código indicando onde uma variável tem **tipo estático diferente de seu tipo dinâmico** (indique quais são os tipos estático e dinâmico da variável neste ponto).

Exemplo de comentário:

```java
  // Passo 5 (c). A variável XXXX abaixo tem tipo estático YYYY e tipo dinâmico ZZZZ.
```

d) Acrescente um comentário no seu código indicando uma chamada de método na qual seja utilizado o conceito de **polimorfismo de método**, e justifique sua resposta.

Exemplo de comentário:

```java
  // Passo 5 (d). A chamada do método XXXX abaixo usa polimorfismo de método porque ...
```
