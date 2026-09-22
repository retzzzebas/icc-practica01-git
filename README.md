# icc-practica01-git
espero que este sea el bueno Lmao

## Preguntas iniciales
1. ¿Qué información almacena un commit?
R: Bytes
2. ¿Qué diferencia existe entre un repositorio local y un repositorio remoto?
R: El local se almacena en tu equipo, el remoto se almacena en la nube 
3. ¿Qué esperan que ocurra cuando ambos integrantes modifican archivos distintos?
R: EL repositorio se va a actualizar con los archivos modificados
4. ¿Qué esperan que ocurra cuando ambos modifican exactamente la misma linea?
R: Solo se modificarà si se guarda el archivo 
## Comandos observados      
git clone
git diff
git add
git commit 
git push
git pull
git status
## planeacion 
A Developer hara los cambios principales 
B Developer hara pequeñas modificaciones y revisara los cambios de A Developer
El push: sera solo cuando los cambios esten verificados
El pull: sera cuando el Depelover A le de luz verde para tener el mismo contenido que el Developer B
## Historial esperado 
A---B---C <- main // Cada lìnea apunta al commit mas reciente, la rama principal se llama main

A---B---C <- main
\
D <- binario // Se crea una nueva historia. ¿Se tratara de un commit nuevo? No se lol

A---B---C <- main
\
D---E <- binario // La linea continua

