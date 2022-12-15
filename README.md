# notion-widgets

<p align="center">
<img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge"/>
</p>

**Olá pessoal!**

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

---

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

Antes de tudo, precisará habilitar o _Github Pages_. Para isso vá até as configurações do seu repositório e em seguida na aba de páginas.
![image](https://user-images.githubusercontent.com/97710656/207861599-1053c769-0e1a-4ca6-ae41-965a3971cbb4.png)

Na parte de Branch, selecione onde o seu widget está.
![image](https://user-images.githubusercontent.com/97710656/207861879-e5730139-b721-462c-8fdb-71965ce72721.png)

Em seguida aperte em salvar.
![image](https://user-images.githubusercontent.com/97710656/207861977-acf1120f-2fbe-4f77-b271-8f929889dc0a.png)

### Passo 4

Vamos utilizar o nosso widget!

Agora você tem acesso ao seus arquivos como em um site. Para conseguir a URL, siga o modelo abaixo.

`usuário.github.io/nome-do-seu-repositório/nome-do-arquivo.html`

**Exemplo**

`akz3ira.github.io/notion-widgets/greatings-hour-dark.html`

E está pronto para ser adicionado em seu notion!

---

Gostaria de sugerir algum Widget novo, encontrou algum BUG ou tem alguma sugestão de alteração? Entre em contato comigo.

<div align="center"> 
  <a href="https://instagram.com/af_designer1/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:afdesigner1@hotmail.com"><img src="https://img.shields.io/badge/Microsoft_Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/afdesigner1/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  <a href="https://www.behance.net/antoniofernand66" target="_blank"><img src="https://img.shields.io/badge/-Behance-blue?style=for-the-badge&logo=behance&logoColor=white" target="_blank"></a> 
  <a href="https://twitter.com/AFDesigner1" target="_blank"><img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" target="_blank"></a> 
 
</div>
