# Git e Github

O curso da  [**codecademy**](https://www.codecademy.com/learn/learn-git) é o mais correto para aprender coisas dos gits, até agora.

[**Git - guia prático**](https://rogerdudler.github.io/git-guide/index.pt_BR.html) bom tbm.

Este documento trata de alguns lembretes para o que vi lá.

---

Dentro da pasta: `git init`

Adicionar para o Index: `git add <arquivo.md> <arquivo.md>` ou `git add *` ou `git add .`

Enviar para o HEAD: `git commit -m "comentários das alterações"`

Discartar as mudanças feitas: `git checkout HEAD <arquivo.md>` ou `git checkout -- <arquivo.md>`

Visualizar as mudanças recentes: `git diff <arquivo.md>`

Discartar mudanças da Stage: `git reset HEAD <arquivo.md>`

Visualizar as mudanças com os IDs: `git log`

Discartar até determinado ponto as mudanças da stage: `git reset <pelo_menos_7_numeros_do_ID>`  
Lembrar de discartar também na pasta de trabalho: `git checkout HEAD <arquivo.md>`

Visualizar qual foi a ùltima mudança feita: `git show HEAD <arquivo.md>`

Mostrar em qual branch você está trabalhando: `git branch`

Criar nova branch: `git branch <nova_branch>`

Modificar qual branch esta usando: `git checkout <nome_branch>`

Fazer merge: `git merge <nome_branch>`  
(Vai pra branch master e executa o comando com o nome da branch em que a modificação está)

Deletar determinada branch: `git branch -d <nome_branch>`  
Caso não tenha sido adicionado a master usar o `-D`

Clonar uma pasta remota: `git clone <pasta_remota> <nome_clone>`

Listar as pastas remotas dos projetos: `git remote -v`

Ver se forma feitas alterações no controle remoto e trazer as alterações para sua cópia local: `git fetch`  
Faz uma ramificação remota com as mudanças

Juntar as coisas de origin para master: `git merge origin/master`

Enviar as coisas de origin para a branch que deseja: `git push origin <branch_name>`


**Isso é tudo pessoal!**