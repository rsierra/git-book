# Capítulo 1 #

## Empezando ##

Este capítulo tratará sobre cómo empezar con Git. Comenzaremos por el
principio, explicando algunos conceptos relativos a las herramientas
de control de versiones, luego pasaremos a ver cómo tener Git
funcionando en tu sistema, y finalmente cómo configurarlo para empezar
a trabajar con él. Al final de este capítulo deberías entender por qué
existe Git, por qué deverías usarlo, y tendrías que tener todo
preparado para comenzar.

## Acerca del control de versiones ##

¿Qué es el control de versiones, y por qué debería importarte? El
control de versiones es un sistema que registra los cambios que se
realizan sobre un archivo a lo largo del tiempo, de modo que puedas
recuperar versiones específicas más adelante. Para los ejemplos de
este libro llevarás control de versiones de código fuente, aunque en
realidad puedes hacer esto con casi cualquier tipo de archivo que
encuentres en un ordenador.

-- Vamos a dejar un espacio aqui, por si se me ocurre algo luego --

Si eres diseñador gráfico o web, y quieres mantener cada versión de
una imagen o diseño (algo que sin duda quieres), un sistema de control
de versiones (Version Control System o VCS en inglés) es una elección
muy sabia. Te permite revertir archivos a un estado anterior, revertir
el proyecto entero a un estado anterior, comparar cambios a lo largo
del tiempo, ver quién modificó por última vez algo que puede estar
causando un problema, quién introdujo un error y cuándo, y mucho más.
Usar un VCS también significa generalmente que si fastidias o pierdes
archivos, puedes recuperarlos fácilmente. Además, obtienes todos estos
beneficios a un coste muy bajo.

### Sistemas de control de versiones locales ###

El método de control de versiones usado por mucha gente es copiar los
archivos a otro directorio (quizás indicando la fecha y hora en que lo
hicieron, si son avispados). Este enfoque es muy común porque es muy
simple, pero también tremendamente propenso a errores. Es fácil
olvidar en qué directorio te encuentras, y guardar accidentalmente en
el archivo equivocado o sobrescribir archivos que no querías.

Para hacer frente a este problema, los programadores desarrollaron
hace tiempo VCSs locales que contenían una simple base de datos en la
que se llevaba registro de todos los cambios realizados sobre los
archivos.
