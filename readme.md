1. 	git reset --hard HEAD~1
2. 	git reflog
#Busco mensaje del commit “Modifico git-nuestro.” Para encontrar identificador de ese commit (1b80fd0)
git branch auxiliar 1b80fd0
#He creado una rama auxiliar con el working copy (es decir con el archivo git-nuestro modificado) antes de hacer el hard reset (paso 11)
git merge auxiliar 
#En ningún momento me había ido de la rama styled por tanto hago un merge para “absorber” la rama auxiliar.
3.   	git merge master 
4.	git checkout styled
git merge htmlify
#Hay conflictos, nos quedamos con el contenido de la rama styled.
5..	git checkout master
git merge styled
#Al hacer cat git-nuestro.md podemos comprobar que el archivo queda como en styled
6. 	git log --graph --decorate --pretty=oneline
7.	git merge --no-f title
8. 	git reset HEAD~1
#Con git status nos damos cuenta de que el working copy no se ha modificado porque hay cambios sin resolver.
9.	git restore <file>
10. 	git Branch -D title
11.	git reflog
#Localizamos el commit antes de hacer el merge
git checkout 756fde7
12. 	git reflog
#Localizamos el commit que pone (initial)
git checkout 2e3c09b
git switch -c inicio
13. 	git reflog
#Localizamos el commit con mensaje “Añado título.”
git checkout 3c30874
git switch -c final
14.  inicio 2e3c09b // styled 1b80fd0 // htmlify a55c23b // title 3c30874

