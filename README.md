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

1. ¿Por qué Git rechazo el primer push de Developer B?
R: Porque el repositorio remoto contiene ahora un commit que no existe en la copia local de Developer B
2. ¿Existía un conflicto de contenido?
R: A lo mejor y si porque editamos la misma linea al mismo tiempo y ambos archivos pertenecian a la misma linea
3. ¿Qué ocurrió cuando ejecutaron pull?
R: Todos los cambios se sincronizaron en ambos Developers
4. ¿Qué diferencia observan entre un push rechazado y un conflicto?
R: El push rechazado pertenece al fallo de hacer cambios al servidor remoto, el conflicto de contenido pertenece a un conflicto en el equipo local

¿Realizar un merge implica necesariamente que exista un conflicto?
R: No porque ya hicimos nuestros propios commit pero en ramas distinitas anteriormente, aparte despues de regresar a la rama main ya actualizamos nuestras copias
e integramos nuestras propias ramas con los cambios ya hechos (al menos podriamos explicarlo asi).

Un merge no decide que una rama tenga “mayor prioridad” que otra. Intenta integrar ambas historias.
R: Pues al parecer es verdad, un merge sirve para integrar el trabajo de ambos para no trabajar sobre la misma linea al mismo tiempo y evitar conflictos de contenido
o push rechazados. No existe la prioridad.

