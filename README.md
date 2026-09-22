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

1. ¿Que representa HEAD en este momento?
R: HEAD representa la version de main de B que intento hacer el merge en main, pero hubo con conflicto
2. ¿Que representa el contenido entre «««< y =======?
R: El mensaje original de Developer A
3. ¿Que representa el contenido entre ======= y »»»>?
R: El contenido modificado por Developer B
4. ¿Por que Git no pudo decidir automáticamente que contenido conservar?
R: Porque trabajamos sobre un solo archivo y no sabe diferenciar entre que modificacion es correcta o incorrecta.

## Historial real
1. ¿En que se parece al dibujo inicial?
R: En absolutamente nada, ya que no sabiamos de que iba a tratar nuestro nuestro historial en realidad, hasta que hicimos git log y nos dimos cuenta que hicimos un 
monton de commit. Bueno, con la excepcion de que existe la rama principal "main" 
y al estar cambiando y creando nuevas ramas, tenian los mismos nombres empleados de "binario" o "decimal" 
2. ¿En que es diferente?
R: En que solo es el dibujo de ejemplo, aqui ya nos dimos cuenta de que va realmente git log, y vimos que hicimos muchas cosas. 
3. ¿Que partes del historial no habían anticipado?
R: No habiamos anticipado que seria tan largo
4. ¿Que entienden ahora que no entendían cuando realizaron el primer dibujo?
R: Entendimos que al hacer varios commits en git, y hacer trabajos remotos, se trata de una gran serie de procesos que estan documentados en el historial y que
no muestran simplemente letritas, hasta los mensajes que dejamos en los commits dejan claro lo que hicimos

¿Que ventaja tiene utilizar el nombre v1.0 para identificar este punto del historial en lugar de utilizar solamente el hash del commit?
R: Discutimos que fue para indicar una version final del repositorio

## Reflexion final
1. ¿Que información almacena un commit?
R: Guardar una snapshot en el staging area, como si fuera un checkpoint
2. ¿Que diferencia existe entre un repositorio local y un repositorio remoto?
R: El local se almacena en tu equipo, el remoto se almacena en la nube
3. ¿Que ocurrió cuando modificaron archivos diferentes?
R: Tras modificarlos en diferentes lineas de desarrollo e integrar esas mismas lineas con los archivos modificados, pudimos integrar los cambios sin conflictos y sin
pedirnos decidir contenido manualmente
4. ¿Que ocurrió cuando modificaron la misma región de un archivo?
R: Aparecio un conflicto de contenido
5. ¿Que diferencia existe entre commit y push?
R: El commit funciona como un checkpoint para el repositorio local, el push sirve para actualizar el repositorio remoto
6. ¿Que función tuvo pull durante la practica?
R: Es basicamente que el otro Developer pueda tener esos mismos cambios que ya se hicieron en el el push
7. ¿Por que un push puede ser rechazado aunque no exista un conflicto de contenido?
R: Porque el repositorio remoto puede contener un commit que no existe en una copia local.
8. ¿Que representa una rama?
R: Representa una linea de desarrollo, como un nombre que apunta a un punto del historial.
9. ¿Que indica HEAD?
R: Indica la rama sobre la que están trabajando actualmente.
10. ¿Que hace merge?
R: Integra los cambios de una rama con otra. Intenta integrar dos historias.
11. ¿Por que Git pudo integrar algunos cambios automáticamente y otros no?
R: Porque los cambios integrados automaticamente venian de diferentes lineas de desarrollo, los que no cumplieron con esto, se debio a que modificamos la misma region
de un mismo archivo
12. ¿Que representan los marcadores «««<, ======= y »»»>?
R: <<<<< Representa la version inicial, ======= separa las versiones, »»»»»» representa la version modificada.
13. ¿Que ventaja proporciona un tag?
R: Permite consultar versiones finales determinadas e identificarlas como puntos especificos del historial
14. ¿Como cambio su interpretación de los diagramas de historial después de utilizar git log–graph –oneline –all?
R: Bastante, nos dieron una mejor vision de todo el trabajo que hicimos y todo lo que documentamos.

¿Por que ambos historiales (merge y rebase)  pueden representar cambios semejantes y, sin embargo, tener una estructura diferente?
R: El merge conserva el historial original intacto y muestra como se unieron las ramas sin alterar los commits existentes, pero un rebase reescribe el historial
por completo a uno lineal, y puede destruir las ramas publicas o compartidas de tus compañeros
