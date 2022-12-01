# projetoComputacao_edsonM
O repositório se trata de um trabalho de projeto semestral da Universidade. Foi realizado o desenvolvimento de um Chatbot com integração ao Telegram (plataforma para troca de mensagens).

PASSOS USADOS PELOS INTEGRANTES PARA EXECUTAR O CÓDIGO

1° PASSO : Instalar o Node (recomendável a versão LTS) pelo site oficial. Pois o nosso projeto foi desenvolvido em JavaScript.
https://nodejs.org/. 

Para conferir a instalação pode-se usar o terminal e digitar os seguintes comandos:

node –version
npm –version


2º PASSO (OPCIONAL): Pode-se instalar o editor de texto VS Code e, dentro do VS Code, instalar o plugin code runner (https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) para simplificar o processo de execução, sendo feito diretamente no VS Code. Quando desejar executar ou para a execução de um código, precisa-se apenas pressionar as teclas:

CTRL + ALT + N     > Executar
CTRL + ALT + M     > Parar execução

3º PASSO: Criar e configurar um Bot no Telegram (Precisa-se instalar o software Telegram, ou usar a versão Web disponível no site oficial https://telegram.org/apps).  

No campo de pesquisa (ícone de lupa), procurar por BotFather. Clicar em BotFather e iniciar a conversa com ele.
.
 (Observação: ele é um bot de respostas automáticas baseado em uma lista de comandos) 

Pressionar o comando no chat ou procurar no menu de comandos ou digitar o comando /newbot para criar um novo bot.


Agora, escolher um nome para o bot e um identificador (finalizando com a palavra bot).

Depois, o bot será criado e informará o Token de acesso ao bot. Este token será usado nos próximos passos. 
É recomendável não compartilhar esse token, pois é um dado sensível.

 
(Observação: Caso alguém tenha acesso a esse dado, há possibilidade dele usar o seu bot. Caso isso aconteça, revogue o seu token de acesso em:
/mybots > identificador do seu Bot > API Token > Revoke Token)

5º PASSO (OPCIONAL):Editar foto de perfil do Bot.
 Para editar a foto volte na conversa com o BotFather, ou procure pelo bot novamente. E realize a seguinte sequência de passos:

/mybots > identificador do seu bot > Edit Bot > Edit Botpic > enviar em anexo a imagem que deseja colocar para o bot.


6º PASSO: Instalar este projeto e as bibliotecas do node para conseguir executar o projeto.

Para baixar o projeto, clique em download ZIP. Depois, extraia a pasta em sua máquina.



Agora, use o terminal e entre dentro do diretório pertencente ao projeto para digitar este comando:

npm i

Se ocorrer qualquer tipo de erro, você poderá instalar cada biblioteca manualmente (dentro do diretório do projeto) com estes comandos:

npm i –save telegraf@3.17.3 -E 

npm i –save axios@0.17.1 -E

npm i –save moment@2.20.1 -E

npm i –save json-server 

Observação: As versões de algumas bibliotecas são declaradas de forma exata para que seja evitado erros devido às novas atualizações de versão delas. 

7º PASSO: Colar seu token de acesso do Telegram no arquivo .env.
Entrar no arquivo .env (através de um editor de texto) na pasta do projeto e trocar seuToken pelo Token do seu bot que colou anteriormente.

(Observação não exclua os apóstrofos, apenas a palavra seuToken) 

8º PASSO: Verificar o seu arquivo package.json.
Na parte de scripts verificar se existe o script “start”: “json-server(…)”

Caso não exista, exclua os scripts existentes e adicione
“start”: “json-server –watch db.json –port 3001”



Assim, poderá ser usado este script através do terminal com o comando npm start para iniciar o servidor através da porta 3001 usando o arquivo db.json para armazenamento (pode alterar a porta ou o arquivo, porém, como padrão, serão utilizados a porta 3001 e o arquivo db.json).

8º PASSO: Executar o código agenda.js e o servidor json server.

8º PASSO (SEM O VS CODE): Se não estiver usando o VS Code, é recomendável abrir dois terminais (um para executar o código e outro para o json server) e, nos dois, entrar dentro do diretório do projeto. Agora, execute o comando npm start no primeiro terminal e depois o comando node agenda.js no outro terminal.

8º PASSO (COM VS CODE): No próprio VS Code com o plugin code runner, é possível usar o terminal disponível no VS (verificar se está dentro do diretório do projeto) e digitar o comando npm start (executar servidor). Depois, pressione as teclas CTRL + ALT + N na aba do arquivo agenda.json (executar código).    



Pronto, agora seu bot estará executando o código e irá armazenar as tarefas no seu arquivo db.json. Agora, procure pelo seu bot no Telegram e divirta-se com ele.


