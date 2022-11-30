# projetoComputacao_edsonM
O repositório se trata de um trabalho de projeto semestral da Universidade. Foi realizado o desenvolvimento de um Chatbot com integração ao Telegram (plataforma para troca de mensagens).

PASSOS USADOS PELOS INTEGRANTES PARA EXECUTAR O CÓDIGO

1° PASSO : Instalar o Node (recomendável a versão LTS) pelo site oficial. Pois o nosso projeto foi desenvolvido em JavaScript.
https://nodejs.org/. 

Para conferir a instalação pode-se usar o terminal e digitar os seguintes comandos:

node –version
npm –version


2º PASSO (OPCIONAL): Pode-se instalar o editor de texto VS Code e, dentro do VS Code, instalar o plugin code runner (https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) para simplificar o processo de execução, sendo feito diretamente no VS Code. Quando desejar executar ou para a execução de um código, precisa-se apenas pressionar as teclas:

CTRL + ALT + N   -> Executar
CTRL + ALT + M   -> Parar execução

3º PASSO: Criar e configurar um Bot no Telegram (Precisa-se instalar o software Telegram, ou usar a versão Web disponível no site oficial https://telegram.org/apps).  

No campo de pesquisa (ícone de lupa), procurar por BotFather. Clicar em BotFather e iniciar a conversa com ele.
.
 (Observação: ele é um bot de respostas automáticas baseado em uma lista de comandos) 

Pressionar o comando no chat ou procurar no menu de comandos ou digitar o comando /newbot para criar um novo bot.


Agora, escolher um nome para o bot e um identificador (finalizando com a palavra bot).

Depois, o bot será criado e será informado o Token de acesso ao bot. 
É recomendável não compartilhar esse token, pois é um dado sensível.

 
(Observação: Caso alguém tenha acesso a esse dado, há possibilidade dele usar o seu bot. Caso isso aconteça, revogue o seu token de acesso em:
/mybots > identificadorBot > API Token > Revoke Token)

4º PASSO: Instalar este projeto e as bibliotecas do node para conseguir executar o projeto.

Para baixar o projeto, clique em download ZIP. Depois, extraia a pasta em sua máquina.



Agora, use o terminal e entre dentro do diretório pertencente ao projeto para digitar estes comandos:

npm i –save telegraf@3.17.3 -E (biblioteca que simplifica o desenvolvimento de bots do Telegram e também é usada para acessar a API do Telegram).

npm i –save 

npm i –save

Observação: As versões de cada biblioteca estão sendo declaradas de forma exata para que seja evitado erros devido às novas atualizações de versão delas. 

5º PASSO: 

