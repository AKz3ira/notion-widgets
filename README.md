# notion-widgets
---

Olá pessoal!

Esse projeto é um teste para usar widgets _self-hosted_ no Notion.
Tenho o intuito de adicionar cada vez mais widgets por aqui então não é um projeto que ficará parado.

---

## Como Utilizar os Widgets

Para utilizar é muito simples. Copie o endereço abaixo:

`https://akz3ira.github.io/notion-widgets/`

e adicione o nome do arquivo do widget que deseja no final dele.

**Exemplo:**

`https://akz3ira.github.io/notion-widgets/greatings-hour-dark.html`

E cole esse link no Notion utilizando o `/Embed` ou cole diretamente como texto e selecione a opção `Create Embed`.

## Gostaria de Personalizar o Meu Widget

### Passo 1

Com uma conta do Guthub, crie um novo Repositório:
![image](https://user-images.githubusercontent.com/97710656/207858627-deedbd11-b2d0-422e-a24e-d21e772fccf5.png)

Adicione um nome e o deixe público. Não precisa alterar mais nada.
![image](https://user-images.githubusercontent.com/97710656/207858807-f63911c6-cc7a-4a1e-a082-886cdde3bacb.png)

### Passo 2

Dentro do Repositório, crie um um novo arquivo.
![image](https://user-images.githubusercontent.com/97710656/207859469-9ec7cd7f-0876-4d8d-a1bf-9ee982bb0978.png)

Dê um nome ao seu arquivo e coloque no final a extensão `.html`.
![image](https://user-images.githubusercontent.com/97710656/207859681-6efb71f8-a7cd-4190-95a0-3349a7c54635.png)

Crie seu widget à vontade no espaço que foi disponível, utilizarei o exemplo do widget de saudações.

```html
<html> 
<head>
    <title>Mensagem de Saudação</title> 
    <style>
#lbl {
    font-family: monospace;
    font-size: xx-large;
    color: white;
    padding: 5px;
    border: 1px solid #ececec;
    text-align: center;
    line-height: 1.5;
    height:85%


}
#date{
    font-size:large;
}
body{
    background-color: #191919;
}
    </style>
</head>
<body>
    <div id="lbl"></div>
</body>

<script>
    var weekday = new Array(7);
    weekday[0] = "Doming";
    weekday[1] = "Segunda";
    weekday[2] = "Terça";
    weekday[3] = "Quarta";
    weekday[4] = "Quinta";
    weekday[5] = "Sexta";
    weekday[6] = "Sábado";

    
    var today = new Date();
    var hrs = today.getHours();
    var dayOfWeek = weekday[today.getDay()];
    var date = dayOfWeek+" " + today.getDate() + "/" +(today.getMonth()+1) +'/'+today.getFullYear()  ;

    var greet;

    if (hrs < 12)
        greet = 'Bom Dia  ';
    else if (hrs >= 12 && hrs <= 18)
        greet = 'Boa Tarde ';
    else if (hrs >= 18 && hrs <= 24)
        greet = 'Boa Noite  ';

    document.getElementById('lbl').innerHTML =
        greet+="Seu Nome Aqui " +`<div id="date"> Hoje é ${date}</div>`;
</script> 
</html>

```

Copie o código acima e cole no seu arquivo. A partir daqui, você poderá personalizálo como preferir e salve ele pelo botão `Commit new file`.

![image](https://user-images.githubusercontent.com/97710656/207860682-f953bd53-4946-4b9a-a6e0-b62c927a8ef3.png)

### Passo 3

Chegou a hora de publicar o seu widget para poder utilizar!

Antes de tudo, precisará habilitar o _Github Pages_. Para isso
