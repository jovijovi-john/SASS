SASS(Syntactically Awesome Style Sheets)

    É uma maneira de "programar" o arquivo de estilo (css com super poderes).

    O SASS funciona de forma pré-processada, quer dizer que você não irá utilizar o arquivo em produção, ele será processado para a utilização final no seu arquivo css. 

    escrevemos os códigos em SASS -> Processado -> Arquivo final (que será utilizado no site)

    .sass (suportada mas não é mais a padrão)

        sintaxe por identação
        
        $cor: blue
        h1
            color: $cor

    .scss (sassy css) e tem como diferencial aceitar css no mesmo arquivo SASS

        $cor: blue;
        h1 { 
            color: $cor 
            }
         
    Por que usar?

        * Objetivo:
            -> Velocidade
            -> Separação facilitada dos arquivos (obtendo uma melhor organização)

        * Recursos:
            -> Variáveis
            -> Operadores
            -> Funções internas
            ...

    Rivais:

        -> Less
        -> Stylus


    Instalação::

        1-> https://sass-lang.com/install
        2-> instalar o npm
        3-> npm install -g sass