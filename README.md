# vim-howtos

Lo fundamental que hay que saber es que para entrar al modo de comandos de Vim hay que pulsar : y no lo olvides porque en Vim lo usarás mil y una veces. En este modo se escriben los comandos y se ejecutan pulsando enter. También hay otro modo de comandos especializado en búsquedas, el cual se activa desde el modo normal pulsando /, pero hablaremos de él en detalle en otra ocasión. Desde este modo también podremos abrir pestañas, ventanas y manejar diferentes archivos, pero eso lo veremos en los próximos posts.

:[rango]d[elete] borra las líneas especificadas.
:[rango]y[ank] copia líneas.
:[línea]put pega el texto en la línea descrita.
:[rango]co[py] {dirección} copia líneas especificadas debajo de la dirección. También se le invoca pulsando :t.
:[rango]m[ove] {dirección} mueve líneas especificadas a la dirección elegida.
:[rango]j[oin] junta líneas.
:[rango]norm[al] {comando} ejectuda comandos del modo normal en las líneas especificadas.
:[rango]s[ubstitute]/{pattern}/{string}/[flags] Reemplaza las ocurrencias de {pattern} con {string} en cada línea especificada.
:[rango]g[lobal]/{pattern}/[comando] ejecuta un comando en cada línea especificadas que coincidan pon el patrón de búsqueda {pattern}.
:[rango]p[rint] su misión es mostrarnos el rango, perfecto para practicar.
:h [comando] información detallada de cada comando.
En la lista anterior, podemos ver diferentes comandos que podemos ejecutar. Es importante saber que no hace falta que escribamos la palabra completa. En el caso de delete podremos usar solo d, y en el de normal podríamos usar solo norm. En cuanto al rango de alcance de nuestro comando, tendremos que aprender a definirlo. Para ello hay que aprender como denomina Vim a las posiciones en cuanto a la línea de comandos (como podéis ver es diferente del modo normal):

1 primera línea del arhivo.
$ última línea del archivo.
0 línea encima de la primera (no existe la línea 0), se usa para mover o pegar texto encima de la primera línea.
. el punto, es la línea donde está ubicado nuestro cursor.
'm línea que contiene la marca (hablaremos de las marcas más adelante) m.
'< inicio de la seleción visual, '> final de la selección visual. Si seleccionamos unas líneas en el modo visual y seguido pulsamos : se creará el siguiente rango automáticamente: :'<,'>.
% todo el archivo, un atajo para el rango :1,$.

Source: https://hipertextual.com/archivo/2014/10/como-usar-vim-6/
