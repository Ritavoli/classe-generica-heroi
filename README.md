 # DESAFIO - Escrevendo as classes de um Jogo - javascript

 > Este repositório foi criado para resolver a 3ª atividade do Bootcamp Potência Tech iFood - Programação do Zero da DIO.  

## Deve ser utilizado

- Variáveis
- Operadores
- Laços de repetição
- Estruturas de decisões
- Funções
- Classes e Objetos

  
##Objetivo:

Crie uma classe generica que represente um herói de uma aventura e que possua as seguintes propriedades:

- nome
- idade
- tipo (ex: guerreiro, mago, monge, ninja )

além disso, deve ter um método chamado atacar que deve atender os seguientes requisitos:

- exibir a mensagem: "o {tipo} atacou usando {ataque}")
- aonde o {tipo} deve ser concatenando o tipo que está na propriedade da classe
- e no {ataque} deve seguir uma descrição diferente conforme o tipo, seguindo a tabela abaixo:

se mago -> no ataque exibir (usou magia)
se guerreiro -> no ataque exibir (usou espada)
se monge -> no ataque exibir (usou artes marciais)
se ninja -> no ataque exibir (usou shuriken)

## Saída

Ao final deve se exibir uma mensagem:

- "o {tipo} atacou usando {ataque}"
  ex: mago atacou usando magia
  guerreiro atacou usando espada

  
## SOLUÇÃO
 > A seguir é apresentado o código desenvolvido para resolver este desafio. Nesse código é informado uma classe generica que representa um herói de uma aventura.


![image](https://github.com/Ritavoli/classe-generica-heroi/assets/142617833/66386563-1dd5-4b3d-8c36-8942cfc1d69d)

class Heroi {
    constructor(nome, idade, tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo;
    }

    atacar() {
        let ataque;
        switch(this.tipo) {
            case "mago":
                ataque = "usou magia";
                break;
            case "guerreiro":
                ataque = "usou espada";
                break;
            case "monge":
                ataque = "usou artes marciais";
                break;
            case "ninja":
                ataque = "usou shuriken";
                break;
            default:
                ataque = "usou um ataque indefinido";
        }

        console.log(`O ${this.tipo} atacou usando ${ataque}`);
    }
}

const heroi = new Heroi("nome do heroi", 30, "mago");

heroi.atacar();
