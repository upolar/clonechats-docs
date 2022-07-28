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

### Como pegar o chat_id de um grupo/canal?

* Existem várias formas de obter o chat_id de um canal. Mostraremos três delas:
- Usando o telegram client [Kotatogram](https://kotatogram.github.io/download/):
  - Acesse a tela de descrição do canal
  - Copie o `chat_id` que aparece abaixo do nome do canal

- Usando bot Find_TGIDbot:
  - Acesse e inicie bot [@Find_TGIDbot](http://t.me/Find_TGIDbot) ou [@myidbot](http://t.me/myidbot)
  - Encaminhe qualquer postagem do canal para este bot
  - O bot responderá com o ID do remetente da mensagem. Neste caso, o ID do canal.
- Copie o `chat_id` (incluindo o sinal de subtração).

- Pela url de uma postagem (apenas grupos ou canais PRIVADOS!)
    - Clique em uma mensagem do canal ou grupo e vá em `Copiar link da Mensagem`
        - Você terá algo como  "https://t.me/c/1684031683/160"
        - O que nos interessa são os números antes da última barra, ou seja:  `1684031683`

!!! info "IMPORTANTE"
        Vale ressaltar que canais começam com o número '-100'. O Kotatogram e a url da postagem não informam o prefixo '-100' então você deve o digitar manualmente.
        O exemplo acima ficaria:
        `-1001684031683`.
        
> Exemplo de um código de canal: `-1001623956859`

---

## :robot: Bots

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
- Cadastre o bot_token na flag bot_token do arquivo `credentials.py`. Remova o '#' no início da linha.