# Anexo: uso de IA en el código (Entrega 3, Grupo 16)

Herramienta: Claude (Anthropic), modelo Claude Sonnet 5.5, usada con acceso a la carpeta del repositorio. Se usó para modificar el código del prototipo, que está completo en un único archivo, `index.html`.

Primero se le pidió leer el código y revisar la interfaz publicada para contrastar los hallazgos del informe del Grupo 15 con lo que la interfaz hace en realidad. En esa etapa no se modificó ningún archivo.

Luego se le pidió implementar los cambios de mayor prioridad, que quedaron en el commit `32e2ad5`. En la vista Comparar, al cambiar a «Tarjeta de la tienda» se muestra el total anterior tachado, el nuevo total y el ahorro; las celdas que cambian se resaltan un instante; aparecen un aviso y una línea de estado; y la fila «Con tarjeta» indica la tienda y muestra «No aplica» donde la publicación no tiene precio con tarjeta. La decisión guardada recalcula su total, avisa cuando cambió respecto del momento en que se guardó y permite actualizarla; el botón «Cambiar» dejó de borrar la decisión (se elige otra publicación y se conserva el motivo), y «Quitar decisión» pasó a ser una acción aparte con «Deshacer». Las celdas del total incompleto se muestran con color de advertencia, con el texto «Incompleto: falta confirmar …» y una línea «Incluye: …». En Buscar se agregó una barra fija inferior con «N agregadas, máx. 4» y el botón «Comparar», se reemplazó el contador «N de 4» y el botón «Agregada» deshabilitado por «Agregada ✓» con un botón «Quitar» (con «Deshacer»).

Después se le pidió implementar los ajustes menores restantes del informe, que quedaron en el commit `e8b6dce`: modelo y capacidad visibles en cada resultado de búsqueda; filas que difieren con fondo azul neutro y la etiqueta «Difiere» en lugar de rojo con «⚠»; el logo «Compara» como enlace a Buscar; modales que se cierran al hacer clic afuera; el botón «Elegir esta» renombrado como «Guardar como mi elección»; el motivo de la decisión visible también en «Mis comparaciones»; y la etiqueta visible «Qué mostrar:» junto a los botones de información.

Todas las desiciones de los cambios y el que se haría en la página fueron hechas por el grupo, e implementadas a nivel de código por IA.

Los cambios se verificaron con la revisión de sintaxis del script y con pruebas automáticas que simulan los flujos principales (agregar y quitar publicaciones, cambiar el medio de pago, guardar, actualizar y quitar una decisión). Esas pruebas se ejecutaron fuera del repositorio y no forman parte de él.
