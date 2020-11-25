# Práctica GIT

Enunciado de la práctica Full Stack Web Bootcamp X Edición ([versión en PDF](./docs/00-Enunciado-Practica-HTML5-CSS3-WEB10.pdf))

**INFORMACIÓN DE CONTACTO**

    Eva Garcia
    emgg2222@gmail.com
    
## Respuestas 

*¿Qué comando utilizaste en el paso 11? ¿Por qué?*

	git reset --hard HEAD~1	
    con reset voy al commit anterior y con --hard se fuerza a   que se pierdan los datos en el working copy

*¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?*


    - git reflog (para visualizar todos los commits)
    
    Para poder volver a el commit que había deshecho localizo el HASH del commit y hago
    git checkout 'numero_HASH' 
    
    git checkout ed324d3
    Note: checking out 'ed324d3'.

    You are in 'detached HEAD' state. You can look around, make experimental
    changes and commit them, and you can discard any commits you make in this
    state without impacting any branches by performing another checkout.

    If you want to create a new branch to retain commits you create, you may
    do so (now or later) by using -b with the checkout command again. Example:

        git checkout -b <new-branch-name>

    HEAD is now at ed324d3 Incluir cursiva en git-nuestro

    
    
    eva@eva-VirtualBox:~/keepcoding/practicas/practicaGit$ git checkout styled
    Previous HEAD position was ed324d3 Incluir cursiva en git-nuestro
    Switched to branch 'styled'
    Your branch is behind 'origin/styled' by 1 commit, and can be fast-forwarded.
        (use "git pull" to update your local branch)
        
        
        
    eva@eva-VirtualBox:~/keepcoding/practicas/practicaGit$ git pull
    Updating 0d53bf3..ed324d3
    Fast-forward
        git-nuestro.md | 18 +++++++++---------
        1 file changed, 9 insertions(+), 9 deletions(-)
		 


*El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?*
		
    Estando situado en la rama styled, ejecuto git merge master 
    No hay conflicto, no tiene nada que actualizar. En master no se ha modificado el fichero.
			

*El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?*

    Nos situamos en la rama styled   

    git checkout styled    
    git merge htmlify
    
    Sí que causó conflicto, porque el fichero git-nuestro se había modificado en ambas ramas y al hacer el merge no sabe con qué cambios quedarse.



*El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?*
			
    No, ya que al hacer merge de styled a master estamos incorporando los cambios que se han hecho en styled pero en master no se ha modificado este fichero
			
			
*¿Qué comando o comandos utilizaste en el paso 25?*

    git log --graph --pretty=oneline

    Añado un alias git config alias.graph "log --graph --pretty"


*El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?*

    Si, no hay ningún commit que se quedaría por ahí suelto. 

*¿Qué comando o comandos utilizaste en el paso 27?*

    git reset HEAD~1

*¿Qué comando o comandos utilizaste en el paso 28?*
    git checkout .

*¿Qué comando o comandos utilizaste en el paso 29?*

    git branch -D title

*¿Qué comando o comandos utilizaste en el paso 30?* 

    git checkout numero_HASH
    git checkout -b nombre_rama

*¿Qué comando o comandos utilizaste en el paso 32?*

    Usando git reflog busco el primer HASH
    git checkout HASH
    git checkout -b nombre_nueva_rama

*¿Qué comando o comandos utilizaste en el paso 33?*

    Usando git reflog busco el HASH del commit Añadimos titulo a git-nuestro
    git checkout HASH
    git checkout -b nombre_nueva_rama

