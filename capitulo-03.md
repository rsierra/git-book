# Ramificaciones en Git #

Cualquier sistema de control de versiones moderno tiene algún
mecanismo para soportar distintos ramales. Cuando hablamos de
ramificaciones, significa que tu has tomado la rama principal de
desarrollo (master) y a partir de ahí has continuado trabajando sin
seguir la rama principal de desarrollo. En muchas sistemas de control
de versiones este proceso es costoso, pues a menudo requiere crear una
nueva copia del código, lo cual puede tomar mucho tiempo cuando se
trata de proyectos grandes.

Algunas personas resaltan que uno de los puntos mas fuertes de Git es
su sistema de ramificaciones y lo cierto es que esto le hace resaltar
sobre los otros sistemas de control de versiones. ¿Porqué esto es tan
importante? La forma en la que Git maneja las ramificaciones es
increíblemente rápida, haciendo así de las operaciones de ramificación
algo casi instantáneo, al igual que el avance o el retroceso entre
distintas ramas, lo cual también es tremendamente rápido. A diferencia
de otros sistemas de control de versiones, Git promueve un ciclo de
desarrollo donde las ramas se crean y se unen ramas entre sí, incluso
varias veces en el mismo día. Entender y manejar esta opción te
proporciona una poderosa y exclusiva herramienta que puede,
literalmente, cambiar la forma en la que desarrollas.

## ¿Qué es una rama? ##

Para entender realmente cómo ramifica Git, previamente hemos de
examinar la forma en que almacena sus datos. Recordando lo citado en
el capítulo 1, Git no los almacena de forma incremental (guardando
solo diferencias), sino que los almacena como una serie de
instantáneas (copias puntuales de los archivos completos, tal y como
se encuentran en ese momento).

En cada confirmación de cambios (commit), Git almacena un punto de
control que conserva: un apuntador a la copia puntual de los
contenidos preparados (staged), unos metadatos con el autor y el
mensaje explicativo, y uno o varios apuntadores a las confirmaciones
(commit) que sean padres directos de esta (un padre en los casos de
confirmación normal, y múltiples padres en los casos de estar
confirmando una fusión (merge) de dos o mas ramas).

Para ilustrar esto, vamos a suponer, por ejemplo, que tienes una
carpeta con tres archivos, que preparas (stage) todos ellos y los
confirmas (commit). Al preparar los archivos, Git realiza una suma de
control de cada uno de ellos (un resumen SHA-1, tal y como se
mencionaba en el capítulo 1), almacena una copia de cada uno en el
repositorio (estas copias se denominan "blobs"), y guarda cada suma de
control en el área de preparación (staging area):

    $ git add README test.rb LICENSE
    $ git commit -m 'initial commit of my project'

Cuando creas una confirmación con el comando 'git commit', Git realiza
sumas de control de cada subcarpeta (en el ejemplo, solamente tenemos
la carpeta principal del proyecto), y guarda en el repositorio Git una
copia de cada uno de los archivos contenidos en ella/s. Después, Git
crea un objeto de confirmación con los metadatos pertinentes y un
apuntador al nodo correspondiente del árbol de proyecto. Esto
permitirá poder regenerar posteriormente dicha instantánea cuando sea
necesario.
