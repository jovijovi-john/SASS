## ** Criando Projeto Com SASS **

    Documentação: https://sass-lang.com/documentation
    

    abra a pasta do projeto no terminal
    crie um arquivo .sass (baseado em identação)

# para converter sass para scss: (na pasta do projeto no terminal) 
    sass style.sass style.scss

    agora temos o arquivo convertido e temos o arquivo style.scss.map, que diz de onde está sendo convertido o arquivo e para onde ele está indo 

Para declarar uma variável: 
    $variavel: black;

# Converter arquivo SCSS para CSS
    sass style.scss style.css

Para nao precisar converter o scss sempre que quiser fazer uma alteração no css, podemos fazer com que o arquivo scss seja monitorado a cada alteração, e automaticamente ele ser convertido para css:

    sass --watch style.scss:style.css

Para monitorar uma pasta inteira:

    sass --watch sass:css

    assim, cada vez q eu criar ou modificar um arquivo na pasta sass, automaticamente será criado/modificado na pasta css

# Interface

    podemos fazer todos esses comandos via cmd ou podemos fazê-los via interface gráfica.
    No caso usaremos o Koala