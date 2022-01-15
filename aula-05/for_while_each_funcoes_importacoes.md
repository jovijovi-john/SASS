for, while, each, funções e importações

# FOR

    O for é usado da mesma maneira que já conhecemos
    
    through: de 1 ate 3 inclusive o 3
    to: de 1 ate 3, mas nao o inclui o 
    
        
    @for $cont from 1 through 3 {
        .item-#{$cont} {
            background: green;
            margin-bottom: 2px;
        }
    }

# WHILE

    
    $cont: 1;
    @while $cont < 4 {
        .item-#{$cont} {
            background: blue;
            margin-bottom: 2px;
        }

        $cont: $cont + 1;
    }

# EACH

    utilizado para exibição de listas. Podemos criar listas de numeros, cores, etc dentro do sass.

    $lista: green, red, yellow, blue;

    $cont: 1;
    @each $cor in $lista {

        .item-#{$cont} {
            background: $cor;
            margin-bottom: 2px;
        }
        $cont: $cont + 1;
    }

# FUNCTION

    @function nomeDaFunction($param: default) {
        ...codigos
    }

    a diferença de uma função pra um mixin é que a função retorna algo, já o mixin faz algum processamento interno mas não retorna nada.

    $total: 12;

    @function largura-coluna($coluna) {
        @return ($coluna/total)
    }

# FUNCOES NATIVAS

    percentage()

# OUTRAS FUNÇÕES 

    ---------------------- função mix -----------------------:
    
    .alerta {
        background: mix(green, orange, porcentagem_de_mistura);
        color: yellow;
    }

        
    .alerta {
        background: mix(red, blue, 30%);
    }

    quanto mais proximo de 100, mais proximo da primeira cor, quanto mais proximo de 0, mais proximo da segunda cor

    ---------------------- função darken -----------------------:

    a função darken deixa a cor mais escura

    darken(cor, porcentagem_de_escurecimento)

    onde porcentagem_de_escurecimento == 1 é black

    ---------------------- função lighten -----------------------:
    
    inverso da função darken

# IMPORTAÇÕES

    para nao criar um arquivo css, criar apenas o scss, basta colocar um underline no inicio do nome do arquivo. Assim, teremos um arquivo partials

    pesquisar sobre mixins:
        copiar os mixins da internet, criar um arquivo _mixins.scss e utilizar esse arquivo que não vai gerar um css e podemos utiliza-los apenas dentro dos nossos arquivos
    
    @import "_endereco_do_arquivo"
    não é necessario colocar o _ na frente de arquivos partials, mas se colocar nao vai ter problema (na importação).