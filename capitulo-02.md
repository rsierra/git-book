# Fundamentos de Git #

Si sólo puedes leer un capítulo para empezar a trabajar con Git, es
éste. Este capítulo cubre todos los comandos básicos que necesitas
para hacer la gran mayoría de las cosas a las que vas a dedicar tu
tiempo en Git. Al final del capítulo, deberías ser capaz de configurar
e inicializar un repositorio, comenzar y detener el seguimiento de
archivos, y preparar (stage) y confirmar (commit) cambios. También te
enseñaremos a configurar Git para que ignore ciertos archivos y
patrones, cómo deshacer errores rápida y fácilmente, cómo navegar por
la historia de tu proyecto y ver cambios entre confirmaciones, y cómo
enviar (push) y recibir (pull) de repositorios remotos.

## Obteniendo un repositorio Git ##

Puedes obtener un proyecto Git de dos maneras. La primera toma un
proyecto o directorio existente y lo importa en Git. La segunda clona
un repositorio Git existente desde otro servidor.

### Inicializando un repositorio en un directorio existente ###

Si estás empezando el seguimiento en Git de un proyecto existente,
necesitas ir al directorio del proyecto y escribir:

    $ git init

Esto crea un nuevo subdirectorio llamado .git que contiene todos los
archivos necesarios del repositorio — un esqueleto de un repositorio
Git. Todavía no hay nada en tu proyecto que esté bajo seguimiento.
(Véase el Capítulo 9 para obtener más información sobre qué archivos
están contenidos en el directorio `.git` que acabas de crear.)

Si deseas empezar a controlar versiones de archivos existentes (a
diferencia de un directorio vacío), probablemente deberías comenzar el
seguimiento de esos archivos y hacer una confirmación inicial. Puedes
conseguirlo con unos pocos comandos `git add` para especificar qué
archivos quieres controlar, seguidos de un `commit` para confirmar los
cambios:
  
    $ git add *.c
    $ git add README
    $ git commit –m 'versión inicial del proyecto'

Veremos lo que hacen estos comandos dentro de un minuto. En este
momento, tienes un repositorio Git con archivos bajo seguimiento, y
una confirmación inicial.
