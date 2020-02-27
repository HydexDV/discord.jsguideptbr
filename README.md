# Como posso fazer meu primeiro bot?

- É necessario instalar um editor de texto com terminal (EX: VS Code)
- Instalar o package do discord.js
- Criar seu bot no DevPortal [Clique Aqui](https://discordapp.com/developers/applications)
# Baixando Visual Studio Code

Acesse o site [Clique Aqui](https://code.visualstudio.com/) e baixe o VSC
Execute o setup e siga as instruções!

# Criando sua application no devPortal

É Necessario criar seu bot no devportal do discord, é bem simples e ja possui um github explicando por imagem logo não sera necessario criar um novo (pReGuIçA)
[Siga os passos](https://github.com/reactiflux/discord-irc/wiki/Creating-a-discord-bot-&-getting-a-token) 

# O Começo

Crie os arquivos necessario para começar a programar o seu bot.
![Alt text](https://cdn.discordapp.com/attachments/682575921727012902/682609370244055055/unknown.png "Title")
##### Adicione esse text no package.json
```json
{
    "name": "nomdedoseubot",
    "version": "1.0.0",
    "description": "descricao",
    "main": "index.js",
    "scripts": {
    },
    "author": "",
    "dependencies": {
      "discord.js": "^11.3.2"
    }
  }
```

##### Adicione isso ao index.js 
```js
const Discord = require("discord.js");
const client = new Discord.Client();
const talkedRecently = new Set();

client.on("ready", () => {
  console.log(
    `---------------------------------\n BOT ONLINE \n---------------------------------`
  );
});
client.on("message", async message => {
  let messageArray = message.content.split(" ");
  let cmd = messageArray[0];
  let args = messageArray.slice(1);
  
//Seus comandos iram aqui 

});
client.login("TOKEN DO SEU BOT");
```

# Usando o Visual Studio Code
- Abra a pasta no qual criou os arquivos do bot!

![Alt text](https://cdn.discordapp.com/attachments/682602203374157886/682711931064287334/unknown.png "Title")

- Selecione o arquivo index.js

![Alt text](https://cdn.discordapp.com/attachments/682602203374157886/682712117249441813/unknown.png "Title")

- Abra o terminal e digite:
```js
npm install discord.js
```
- Apos Finalizar a instalação digite
```js
node .
```
Caso apareça essa mensagem você conseguiu colocar seu bot online!
![Alt text](https://cdn.discordapp.com/attachments/682602203374157886/682713077523021857/unknown.png "Title")

# PROXIMO TUTORIAL: SEUS PRIMEIROS COMANDOS
