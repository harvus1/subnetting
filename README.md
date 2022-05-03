###SUBNETTING

Subnetting hace referencia a la subdivisión de una red en varias subredes. El Subneteo permite a los administrados de red poder dividir una red empresarial en varias subredes sin hacerlo público en internet. Esto se traduce en que el router que establece la conexión entre la red e internet se especifica como dirección única. Aunque puede que haya varios hosts ocultos. Así el numero de hosts que está a disposición el administrador aumenta considerablemente.

# Objetivos

Como parte del proyecto de aplicación de este curso decidimos tomar en cuenta el utlimo tema visto en clase, que es enfocado en las redes, de mas manera mas especifica en el Subneteo. Consideramos este tema ya que es un tema bastante importante dentro del ámbito de las redes y de la misma manera es una de las bases del curso de redes por lo que es mejor irse familiarizando con este tipo de temas. Es un proceso no tan complicado, tiene un pequeño grado dificultad y es un proceso que se puede considerar algo largo de realizar ya que si se realiza a mano nos puede tomar bastante tiempo por lo que decidimos automatizar ciertos procesos.

#Como funciona el subnetting?

En el subnetting o subneteo se toman bits del ID del host “prestados” para crear una subred. Con solo un bit se tiene la posibilidad de generar dos subredes, puesto que solo se tiene en cuenta el 0 o el 1. Para un número mayor de subredes se tienen que liberar más bits, de modo que hay menos espacio para direcciones de hosts. Cabe remarcar en este caso que tanto las direcciones IP de una subred como aquellas que no forman parte de ninguna tienen la misma apariencia y los ordenadores tampoco detectan ninguna diferencia, de ahí que se creen las llamadas máscaras de subred. Si se envían paquetes de datos de Internet a la propia red, el router es capaz de decidir mediante esta
máscara en qué subred distribuye los datos. Como ocurre con las direcciones de IPv4, las máscaras de red contienen 32 bits (o 4 bytes) y se depositan en la dirección como una máscara o una plantilla. Una típica máscara de subred tendría la siguiente apariencia: 255.255.255.128

Esto también puede representarse de forma binaria: 11111111.11111111.11111111.10000000

Para la comparación se supone que la combinación de dos unos en la misma posición vuelve a dar un uno como resultado. El resto de comparaciones (1/0, 0/1 y 0/0) dan 0 como resultado. (Esta comparación no es un proceso en el que tú seas el único participante, sino que el router también realiza los cálculos).
La comparación AND arroja la dirección de red. Para la dirección del host se tienen en cuenta todas las posiciones que aparecen en el lado derecho de los ceros, como en nuestro ejemplo:

- Dirección IP: 192.168.88.3
- Net ID: 192.168.88.0
- Host ID: 0.0.0.3

[![Subnetting](https://www.cspsprotocol.com/wp-content/uploads/2019/12/Subnetting-Explained-With-Example.png "Subnetting")](https://www.cspsprotocol.com/wp-content/uploads/2019/12/Subnetting-Explained-With-Example.png "Subnetting")
