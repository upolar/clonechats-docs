# Perguntas Frequentes

Aqui estão separadas algumas das perguntas mais feitas.

--- 

## Geral

### O que é e para que serve?

O clonechat é um programa que auxilia na clonagem de canais e grupos. É uma forma de criar um backup seguro de canais ou grupos que podem ter suas mensagens deletadas.

### Funciona em canais com encaminhamento desativado? 

Não. Para fazer o backup de canais/grupos nessa situação é preciso baixar o conteúdo e usar outro programa para envia-los, como o zipsender ou o zimatise.

### Existe risco de usar o clonechat? Se sim, quais?

**Não e sim**. O clonechat vem configurado com um tempo de envio entre cada mensagem de `10 segundos` para evitar problemas. Além disso recomendamos uma clonagem de até 1000 postagens no modo usuário por dia. Não recomendamos deixar o tempo menor que 10 segundos!

### Consigo copiar canais com compartilhamento restrito?

**Não**. O clonechat funciona com o princípio de encaminhar mensagens de um canal/grupo para outro, se não for possível encaminhar mensagens do chat de origem você terá que baixar todos os arquivos e upa-los para o Telegram com outro programa.

---

## Grupos e canais

### Como pegar o chat_id de um grupo/canal?

Existem várias formas de obter o chat_id de um canal. Mostraremos três delas:
#### 
- [Usando um app não oficial](#usando-um-app-nao-oficial): Para computador.
- [Usando um bot](#usando-um-bot): Computador & celular.
- [Pelo link da postagem](#pela-url-de-uma-postagem): Computador & celular. Funciona apenas para grupos/canais PRIVADOS!

#### Usando um app não oficial
!!! tip "IMPORTANTE"
        Vale ressaltar que canais começam com o número '-100'. O Kotatogram e a url da postagem não informam o prefixo '-100' então você deve o digitar manualmente.

- Usando o [64Gram](https://github.com/TDesktop-x64/tdesktop/releases):

    - Em `Assets` você verá algumas opções de download. Se você estiver no Windows toque em uma das opções em que o nome termina com `.exe`;
    - Instale e faça login na sua conta; e, por fim:
    - Abra o canal que deseje ver o ID, toque em seu nome para ver as informações do canal e copie o ID do canal (channel id).

<br>

- Usando o [Kotatogram](https://kotatogram.github.io/download/):
    - Baixe e instale;
    - Abra o canal e clique em seu nome para abrir as informações do canal; e, por fim:
    - Copie o `chat_id` que aparece abaixo do nome do canal

#### Usando um bot

- Acesse e inicie o bot [@myidbot](http://t.me/myidbot)
- Encaminhe qualquer postagem do canal ou grupo para este bot. No caso de grupos você precisa encaminhar a mensagem de um administrador anônimo OU pegar o id usando o [computador](#usando-um-app-não-oficial-computador).
- O bot responderá com o ID do remetente da mensagem. Neste caso, o ID do canal.
- Copie o `chat_id` (incluindo o sinal de subtração).

#### Pela URL de uma postagem
!!! tip "IMPORTANTE"
        Vale ressaltar que canais começam com o número '-100'. O Kotatogram e a url da postagem não informam o prefixo '-100' então você deve o digitar manualmente. 
- Pela url de uma postagem (apenas grupos ou canais PRIVADOS!)
    - Clique com o botão direito (computador) ou toque na mensagem (celular) em uma mensagem do canal/grupo e vá em `Copiar link da Mensagem`
        - Você terá algo como  "https://t.me/c/1684031683/160"
        - O que nos interessa são os números antes da última barra, ou seja:  `1684031683`
        - Como o ID que eu copiei acima é de um canal é preciso adicionar o -100, então o ID CORRETO do canal ficaria: `-1001684031683`.

---

## Bots :robot:

### O que é um bot token e por que usar?

Bot token é a credencial de acesso para controlar um bot de telegram.

O encaminho de mensagens por bot é mais rápido. O telegram limita a permissão sobre volume de postagens de forma diferente entre a interface de usuário e a interface de bots. Para manter a segurança e ficar livre de punições do telegram, é recomendável que a conta do usuário não encaminhe mais que 6 mensagens por minuto. Já para bots, o limite sobe para 60 mensagens por minuto. Assim, o Clonechat opera 10 vezes mais rápido quando em `mode=bot`.

O uso em modo bot possui algumas exigências:

- No arquivo `config.ini`, a flag `mode` precisa ser alterada para `bot`
- O bot precisa ser administrador do canal de origem
- Sua conta do telegram precisa fazer parte do canal de origem

### Como gerar o token e ativar?

Geração:

  * Abra seu app do Telegram, busque por: @BotFather e clique sobre ele;
  - Envie o comando: `/newbot`;
  - Insira um nome para o seu bot;
  - Insira um username. O username obrigatoriamente tem que terminar com a palavra bot. Ex: eusouumbot, tambemsouum_bot.
  - Feito isso, você receberá o código bot_token.

Ativação:

- Edite o arquivo `credentials.py`.
- Remova o '#' do inicio da linha do bot_token. Se atente a não deixar um espaço antes de bot_token.
- Troque os "bbbbbbbbbbbbb" pelo seu token gerado acima. 