# RepoGitHenry
Posgrado UCEM.

  465  git remote -v
  466  git remote add https://github.com/mgarciaf/calculadora.git
  517  git log --oneline --pretty=format:'%h %an %s'
  518  git log --oneline --pretty=format:'%h   %an   %s'
  519  git log --oneline --pretty=format:"%h   %an   %s"
  520  git config --list | grep alias
  521  git config --global alias.loghenry 'log --oneline --pretty=format:"%h  %an  %s"'
  522  git loghenry
  523  git config --list | grep alias
  524  history
  
  Crear rama apartir del stash
  497  git stash save -u "nuevo_stash"
  498  git stash list
  499  git stash branch rama_segun_stash stash@{0}
  501  git stash save -u 'otro_nuevo_stash'
  502  git stash apply

Fusionando 2 cambios en un solo commit.
  526  nano Prueba.txt
  527  git status
  528  git add .
  529  git status
  530  git commit -m "Creacion"
  531  ls
  532  nano Prueba.txt
  533  git status
  534  git add .
  535  git status
  536  git commit --amend -m "Mismo commit incluyendo 2 cambios"
  537  git log --oneline --pretty=format:'%h   %an   %s'

# Perdemos lo que hayamos hecho
git reset -hard origin/master

# cuando tenemos los cambios en el local
git reset HEAD~1
#cuando ya tenemos nuestros cambios arriba (git commit y git push)
git commit -am "agregar cambio"
git revert 

Cuando ya hicimos push, no usar el reset, para no alteral el grafico historico, se debe usar el REVERT.
Igualar la rama remota a la local
git reset --hard origin nuevarama

#Inserta un commit especifico en una nueva rama
git cherry-pick a8hh88aa8

git tag v1.0
git tag -a v1.1 -m "Comentario"
git push origin v1.0
git push origin --tags
git tag -d v1.0
