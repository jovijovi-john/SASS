Mixin, Herança e Diretivas de Controle

    *Mixin*

        Serve para reaproveitar codigos css que se repetem diversas vezes

        @mixin titulo {
            padding: 10px 5px;
            background: rgb(255, 153, 0);
        }

        h1 {
            color: white;
            margin-bottom: 10px;
            @include titulo;
        }

        h2 {
            color: rgb(0, 0, 0);
            @include titulo;
        }

    os valores padrão sao sempre contados do final para o começo. Logo se colocar
     
    @mixin titulo (@param1: default, @param2) {}
    vai dar erro


Multiplas Diretivas é quando uma classe herda de mais de uma classe, exemplo:
        
    .classe-1 {
        color: red;
    }

    .classe-2 {
        background: black;
    }

    .vermelho{
        @extend .classe-1;
        @extend .classe-2;
        font-weight: bold;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        padding: 20px;
    }

E se eu nao quiser criar a classe pai e a classe filha? ter elas apenas para estabelecer a relação de herança. O nome disso é PLACEHOLDER. Basta colocar % antes do nome da classe

# Diretivas de controle (condicionais)

/* Diretivas de Controle */

$cor: green;
@if ($cor == green) {
    p {
        color: $cor;
    }
}@else if ($cor == red){
    p {
        color: $cor;
    }
}@else {
    p {
        color: black;
    }
}