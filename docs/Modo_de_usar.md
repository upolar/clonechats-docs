# Modo de Usar
!!! note ""
    === "Menu (Windows)"
        ## Iniciando
        
        * Digite o chat_id do canal/grupo de origem.
        
        !!! faq "Pegando o chat_id de um canal/grupo"
                Leia a nossa seção de [como pegar o chat_id de um grupo/canal](./perguntas-frequentes.md#como-pegar-o-chat_id-de-um-grupocanal) nas Perguntas Frequentes. 

        - Confirme com [ENTER]
        - Digite o chat_id do canal/grupo de destino (o canal onde deseja salvar as mensagens)
        - Confirme com [ENTER]


        ### Escolher os tipos de arquivos a serem clonados

        Após confirmar o id de origem e o id de destino aparecerá um menu para filtragem.

        - Digite uma opção de filtro de arquivos dentre as disponíveis.
        ```
        0 - Clona todos os arquivos
        1 - Fotos
        2 - Apenas texto
        3 - Documentos (pdf, zip, rar, ...)
        4 - Stickers/figurinhas
        5 - GIF's
        6 - Arquivos de áudio (música)
        7 - Mensagens de voz
        8 - Vídeos
        9 - Enquetes
        ```
        - Se quiser clonar todos os arquivos digite o número zero `0`.
        - Você pode selecionar múltiplas opções as separando com vírgulas. Ex.: `1,3` para clonar apenas fotos e documentos.

        * Informe se deseja iniciar uma nova clonagem ou continuar uma clonagem iniciada anteriormente
            - Digite `1` para iniciar uma clonagem do zero.
            - ou `2` para continuar uma clonagem já iniciada
            - Confirme com [ENTER]

    === "Terminal"

        Abra o terminal do Windows ou Linux na pasta do clone chat e digite o comando abaixo.

        > python clonechat.py --orig={chat_id do canal/grupo de origem} --dest=-{chat_id do canal/grupo de destino}``

        Exemplo: `python clonechat.py --orig=-100222222 --dest=-10011111111`

### Fazendo login

Na primeira vez que você for usar, será preciso autenticar uma conexão com o Telegram. Mas será só da primeira vez! E depois nunca mais. :) Autenticar é simple, segue os passos:

> `"Enter phone number or bot token:"`

- Aparecerá esta mensagem pedindo o número de seu telefone em formato internacional.
- Digite seu número de telefone com prefixo `+55` para o caso de telefone brasileiro, seguido do DDD local e seu número de telefone.
- Exemplo: Para telefone de São Paulo, com ddd 11, deverá ser digitado algo como: `+5511995429405`
- Na mensagem perguntando se o número está correto, digite `y`.
- Será enviado um código para seu telegram, que você deve digitar no terminal.
- Por fim, se você tiver 'segurança de 2 fatores' (2fa) ativado na sua conta, será solicitado sua senha.
Aguarde a clonagem terminar!

!!! info "Importante"
        Clonagem via usuário (mode=user) possui uma pausa de 10 segundos entre posts. Já clonagem via bot (mode=bot) é mais rápido, possuindo uma pausa de apenas 1 segundo entre posts.

Se tudo estiver certo nesse momento a clonagem vai se iniciar.
