<div>
  <img style="100%" src="https://capsule-render.vercel.app/api?type=waving&height=80&section=header&reversal=false&fontSize=70&fontColor=FFFFFF&fontAlign=50&fontAlignY=50&stroke=-&descSize=20&descAlign=50&descAlignY=50&theme=tokyonight"  />
</div>

# Resultados curso udemy "Git Completo: Do Básico ao Avançado" concluído em 02/26.
## O texto abaixo é uma mostra parcial do que aprendi ao concluir o curso acima citado (todos os comandos foram utilizados para construir esse repositório).

_**Os comando abaixo foram replicados no git Bash**_

**Configurações básicas**

```
 git config --global user.name meu_nome
 git config --global user.email meu_email
 git config --global core.editor "code --wait"
 git remote add server https://github.com/rodrigonsv5148/Git-Github_Pratica.git
```

```
git init (criar o repositório)
```

**Foram criados**
   - **3 arquivos .txt no repositório**
   - **.gitignore**
   - **_README.MD_**

```
 git status - retornou que estão untracked
 git add .
 git commit -m "Commit inicial"
 git push --force --set-upstream server main ("force" por conta do commit inicial do GitHub já ter uma hash diferente da local (poderia 
 ter clonado o repositório antes de colocar os arquivos para evitar esse problema mas vou deixar para depois a título de experiencia)).
```

**Alterei um arquivo**

```
 git status - acusou Arquivo 1.txt modificado
 git diff 'Arquivo 1.txt' - vejo as modificações especificamente do arquivo
 git fetch
 git commit -a -m "Arquivo 1 modificado com sucesso"
 git push
 clear

 git branch dev2
 git switch dev2
```

**Alterei o Arquivo 2.txt**

**Fiz um commit na branch dev2 (não repetirei comandos relacionados a processos como "commit" para ficar mais simplificado)**

**Voltei para a main**

```
 git switch -c branchNaoFuncional
 git push --set-upstream server branchNaoFuncional (me arrependi da existência dessa branch)
 git switch -
 git push --delete server branchNaoFuncional
 git branch -d branchNaoFuncional
```

**Fiz um commit com intuito de gerar conflito na alteração que eu fiz com a branch**

```
 git merge dev2
```

**Resolvi o conflito**

```
 git merge --continue
 git push
 git branch --merged (confirmando que a branch foi mesclada corretamente)

 git tag conflito (não gostei do nome)
 git tag -d conflito
 git tag tag_1
 git push server tag_1
```

**Criei um commit, mexi nele mas percebi que esse commit deveria ser desfeito mas mantendo as alterações**

```
 git reset --mixed MAIN~1
```

**Fiz um commit novamente com todas alterações**

**Criei uma branch, e percebi que teria que voltar a trabalhar na branch main, mas não quero perder as modificações nem fazer um commit de algo incompleto**

```
 git stash
 git checkout main
 git stash --list
 git stash apply stash@{0} (usei stash invés de merge apenas para exemplificar)
```

**Busquei atualizações com fetch, criei e enviei uma branch (dev4) para aplicar os conceitos de rebase (para trocar a base de uma branch e o commit não gerar um merge commit) e cherry pick (para colocar um commit de uma brach como o commit mais atual de outra)**

```
 git rebase main
```

**resolvi o primeiro conflito**

```
 git rebase --continue
```

**resolvi o segundo conflito**

```
 git rebase --continue
 git switch -
 git merge dev4
 git push
```

**Não retirarei a branch remota dev4 por questões de visualização do trabalho**

```
 git log --oneline --all --graph ( Para que eu possa escolher a hash correta do cherry pick )

 git cherry-pick 6f27dab
```

**Corrigido o conflito**

```
 git cherry-pick --continue
 git commit --allow-empty (visto que a branch main já possuía a modificação feita nesse commit por conta do rebase+merge anterior)
```

**Para finalizar, dei um push resultando nesse repositório que você está acessando**

```
 rm -rf .git
```

**Depois deletei a pasta, abri o gitbash novamente**

```
 git clone https://github.com/rodrigonsv5148/Git-Github_Pratica.git
```

**Existem outros conceitos e comandos que eu gostaria de exemplificar como a busca binária através do comando Bisect, a criação de atalhos com Alias, o retorno ao commits antigos com o checkout, a criação de novos commits baseados em antigos com o git revert, o uso de SSH keys. Porém o texto já ficou muito grande.**

**Em resumo aprendi mais coisas do que mostrei embora tenha consciência que tenho muito a aprender visto que o aprendizado nunca acaba.**

# Resumo do meu estudo 
<img width="2629" height="3341" alt="UDEMY - Programation (1)" src="https://github.com/user-attachments/assets/684512fc-aff6-4a59-9567-c78009ef2229" />

<div>
  <img style="100%" src="https://capsule-render.vercel.app/api?type=waving&height=80&section=footer&reversal=false&fontSize=70&fontColor=FFFFFF&fontAlign=50&fontAlignY=50&stroke=-&descSize=20&descAlign=50&descAlignY=50&theme=tokyonight"  />
</div>
