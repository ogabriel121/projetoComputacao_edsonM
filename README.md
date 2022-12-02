# Projeto JulhoBot - Chatbot do Telegram :speech_balloon:<br><br> <img src="https://user-images.githubusercontent.com/103379267/205323965-1d9a68e8-85b9-4627-8641-0dca46b534d4.jpg" width="125px" />
## O Repositório se Trata de um Trabalho de Projeto Semestral da Universidade. Foi Realizado o Desenvolvimento de um Chatbot para o Telegram (plataforma para troca de mensagens).

* ### *PASSOS PARA EXECUTAR O BOT*

<br>

### **1° PASSO:** Instalar o Node
É recomendável fazer a instalação da versão do tipo **LTS** pelo site oficial. Pois o nosso projeto foi desenvolvido em JavaScript usando Node.
<a href="https://nodejs.org/" target="_blank">Clique aqui para ir ao site do Node</a>

Para conferir a instalação pode-se usar o terminal e digitar os seguintes comandos:

```bash
node –-version
```
```bash
npm –-version
```

<br>

### **2º PASSO (OPCIONAL):** Instalar o VS Code e o Plugin Code Runner 
Pode-se instalar o editor de texto <a href="https://code.visualstudio.com/" target="_blank">VS Code</a> e, dentro do VS Code, instalar o plugin <a href="https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner" target="_blank">code runner</a> para simplificar o processo de execução, sendo feito diretamente no VS Code. 

Quando desejar executar ou para a execução de um código, precisa-se apenas pressionar as teclas:

` CTRL + ALT + N ` -> Executar

` CTRL + ALT + M ` -> Parar execução

<br>

### **3º PASSO:** Criar e Configurar um Bot no Telegram
Para criar e Configurar um Bot no Telegram é necessário instalar o software **Telegram**, ou usar a versão Web disponível no <a href="https://telegram.org/apps" target="_blank">site oficial</a>.  

No Telegram, encontrar o campo de pesquisa (ícone de lupa) e procurar por **BotFather**. Depois, clicar em BotFather e iniciar a conversa com ele.

<div align="left">
<img src="https://user-images.githubusercontent.com/103379267/205319116-636cc425-d96a-44e5-b45a-a74e5750319b.PNG" width="550px" />
</div>

(Observação: ele é um bot de respostas automáticas baseado em uma lista de comandos)

Pressionar o comando no chat ou procurar no menu de comandos ou digitar o comando `/newbot` para criar um novo bot.
<div align="left">
<img src="https://user-images.githubusercontent.com/103379267/205319217-c25104b0-1db9-4d3c-ab69-a9d9a3574a30.PNG" width="550px" />
</div>

Agora, escolher um nome para o bot e um identificador (finalizando com a palavra bot).
(Observação: Guarde o nome e o identificador do bot, será possível encontrar seu bot por meio dos dois)

Depois, o bot será criado e informará o Token de acesso ao bot. Este token será usado nos próximos passos. 
**É recomendável não compartilhar esse token, pois é um dado sensível.**
<div align="left">
<img src="https://user-images.githubusercontent.com/103379267/205319292-2475b99f-7842-4096-a87d-837a1e1c8706.png" width="550px" />
</div>

(Observação: Caso alguém tenha acesso a esse dado, há possibilidade dele usar o seu bot. Caso isso aconteça, revogue o seu token de acesso em: ` /mybots > identificador do seu Bot > API Token > Revoke Token ` )

<br>

### **4º PASSO (OPCIONAL):** Editar Foto de Perfil do Bot

 Para editar a foto volte na conversa com o BotFather, ou procure pelo bot novamente. E realize a seguinte sequência de passos:

` /mybots > identificador do seu bot > Edit Bot > Edit Botpic > enviar em anexo a imagem que deseja colocar para o bot `
<div align="left">
<img src="https://user-images.githubusercontent.com/103379267/205322915-4654fa98-0b87-44f7-9c85-d6949bf18e74.PNG" width="550px" />
</div>

<br>
<br>

### **5º PASSO:** Instalar este Projeto e as Bibliotecas do Node para Conseguir Executar o Projeto

Para baixar o projeto, clique em download ZIP. Depois, extraia a pasta em sua máquina.

<img src="https://user-images.githubusercontent.com/103379267/205360246-f970cc88-64b9-463a-aa23-b6ecc65898e1.PNG" width="380px" />

Agora, use o terminal e entre dentro do diretório pertencente ao projeto para digitar este comando:
```bash
npm i
```

Se ocorrer qualquer tipo de erro, você poderá instalar cada biblioteca manualmente (dentro do diretório do projeto) com estes comandos:

```bash
npm i -–save telegraf@3.17.3 -E
```
```bash
npm i -–save axios@0.17.1 -E
```
```bash
npm i –save moment@2.20.1 -E
```
```bash
npm i -–save json-server
```

Observação: As versões de algumas bibliotecas são declaradas de forma exata para que seja evitado erros devido às novas atualizações de versão delas. 

<br>

### **6º PASSO:** Colar Seu Token de Acesso do Telegram no Arquivo .env
Entrar no arquivo .env (através de um editor de texto) na pasta do projeto e trocar seuToken pelo Token do seu bot que colou anteriormente **(no 3º PASSO)**.

<img src="https://user-images.githubusercontent.com/103379267/205360968-c219cb16-730e-46b9-81f7-8f06a2e4e054.png" width="651px">
(Observação não exclua os apóstrofos, apenas a palavra seuToken) 

<br>

### **7º PASSO:** Verificar o Seu Arquivo package.json
Na parte de scripts verificar se existe o script `"start": "json-server(…)"`

Caso não exista, exclua os scripts existentes e adicione
```json
"start": "json-server –-watch db.json –-port 3001"
```
<img src="https://user-images.githubusercontent.com/103379267/205362379-cfd5c214-3415-4ead-ad03-a83de8506e87.png" width="615px">

Assim, poderá ser usado este script através do terminal com o comando npm start para iniciar o servidor através da porta 3001 usando o arquivo db.json para armazenamento (pode alterar a porta ou o arquivo, porém, como padrão, serão utilizados a porta 3001 e o arquivo db.json).

<br>

### **8º PASSO:** Executar o Código agenda.js e o Servidor json server

**8º PASSO *(SEM O VS CODE)*:** Se não estiver usando o VS Code, é recomendável abrir dois terminais (um para executar o código e outro para o json server) e, nos dois, entrar dentro do diretório do projeto. Agora, execute o comando npm start no primeiro terminal e depois o comando node agenda.js no outro terminal.

<img src="https://user-images.githubusercontent.com/103379267/205374937-4239e50c-6146-418a-afc5-3a434ca5903a.PNG" width="750px">

**8º PASSO *(COM VS CODE)*:** No próprio VS Code com o plugin code runner, é possível usar o terminal disponível no VS (verificar se está dentro do diretório do projeto) e digitar o comando npm start (executar servidor). Depois, na aba do arquivo agenda.js, para executar o código pressione as teclas:

`CTRL + ALT + N`

(Observação: Já foi comentado sobre esse comando no **2º PASSO**)

<img src=""colocar imagem aqui>

<br>
<br>

#### Pronto, agora seu bot estará executando o código e irá armazenar as tarefas no seu arquivo db.json. Agora, procure o seu bot pelo **identificador ou nome**  *(seguindo o mesmo exemplo de procura do 3º PASSO pelo BotFather)* no Telegram e divirta-se com ele.

<img src="https://user-images.githubusercontent.com/103379267/205396495-2cf7b71e-3b5b-4473-ad63-edb44f55cf96.PNG" width="650px">

<br>
<br>

### Espero que tenha gostado do projeto assim como o Octocat!
> ![parabéns](https://media.giphy.com/media/jrdgDVFrcgJpNlonWO/giphy.gif)

<br>

#

<br>

### Referências Utilizadas no Projeto

> Guia de Markdown : https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown#open

> Curso de Chatbot : https://www.cod3r.com.br/courses/chatbot-para-telegram-com-node-3-projetos
