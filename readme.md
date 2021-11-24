1. 	git reset --hard HEAD~1</BR>

2. 	git reflog</BR>
#Busco mensaje del commit “Modifico git-nuestro.” Para encontrar identificador de ese commit (1b80fd0)</BR>
git branch auxiliar 1b80fd0</BR>
#He creado una rama auxiliar con el working copy (es decir con el archivo git-nuestro modificado) antes de hacer el hard reset (paso 11)</BR>
git merge auxiliar </BR>
#En ningún momento me había ido de la rama styled por tanto hago un merge para “absorber” la rama auxiliar.</BR>
3.  git merge master </BR>
4.	git checkout styled </BR>
    git merge htmlify</BR>
#Hay conflictos, nos quedamos con el contenido de la rama styled. </BR>
5..	git checkout master
git merge styled </BR>
#Al hacer cat git-nuestro.md podemos comprobar que el archivo queda como en styled </BR>
6. 	git log --graph --decorate --pretty=oneline </BR>
7.	git merge --no-f title </BR>
8. 	git reset HEAD~1 </BR>
#Con git status nos damos cuenta de que el working copy no se ha modificado porque hay cambios sin resolver. </BR>
9.	git restore <file></BR>
10. 	git Branch -D title </BR>
11.	git reflog </BR>
#Localizamos el commit antes de hacer el merge </BR>
git checkout 756fde7 </BR>
12. 	git reflog </BR>
#Localizamos el commit que pone (initial) </BR>
git checkout 2e3c09b</BR>
git switch -c inicio </BR>
13. 	git reflog </BR>
#Localizamos el commit con mensaje “Añado título.”
    git checkout 3c30874 </BR>
    git switch -c final
14.  inicio 2e3c09b // styled 1b80fd0 // htmlify a55c23b // title 3c30874 </BR>

