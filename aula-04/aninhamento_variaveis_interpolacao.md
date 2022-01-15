## Aninhamento, variáveis e interpolação

    Aprenderemos: Comentários, aninhamento, referenciar seletor pai, variáveis e interpolação

    o sass é uma linguagem de scripts. Na versão mais recente foi escrita usando Dart

# Comentários:

    /**/ ou //

# Aninhamento

    normalmente escreveriamos o codigo assim:

        #conteudo {
            background: $cor;
            padding: 15px;
        }

        #conteudo h1 {
            color: $cor2;
        }

        #conteudo a {
            color: $cor3;
        }
    
    mas no sass, escreveremos de outra forma, colocando itens dentro de outros itens:

        #conteudo {
            background: $cor;
            padding: 15px;

            h1 {
                color: $cor2;
            }

            a {
                color: $cor3;
            }
        }

    para selecionar o seletor pai, basta usar &:

        a {
            color: $cor;

            &:hover {
                color: $cor2;
            }
        }

    é importante comentar que variáveis tem escopo, assim como em linguagens de programação

    para definir uma variavel como global basta usar !global na atribuição
    ex:

    $cor: red;

    p {
        color: $cor; /*red*/
    }

    h1 {
        $cor: blue !global;
        color: $cor; /*blue*/
    }

    h2 {
        $color: $cor; /*blue*/
    }

# Interpolação

    #{$variavel}

    $bg_color: background-color;
    $cor: red;

    h1 {
        #{$bg_color}: $cor;
    }