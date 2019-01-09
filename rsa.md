# Coisas relacionadas ao RSA:

Para gerar e usar sua chave RSA siga o tutorial do Rapha: [**How to use RSA key**](https://gitlab.stilingue.com.br/snippets/110).

 
## RSA parou de funcionar?

1. Remover tudo da pasta `.ssh/environment`:

>```rm -rf .ssh/environment*```

2. Verificar o número do PID do processo `ps`:

>```ps -fp $(pgrep -f ssh-agent)```

3. Matar os processos com o nome ssh-agent:

>```pkill -9 -f ssh-agent```
