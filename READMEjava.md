************************************
ACERCA DEL AUTOR
************************************

David M.

elarreglador@protonmail.cocm

https://github.com/elarreglador


************************************
ACERCA DE LA APLICACION
************************************

Cuando el tratamiento del servidor a los clientes requiere un proceso complejo, se requerirá la creación de hilos para atender las peticiones. Por eso el servidor será multihilo, creará un hilo de trabajo para cada cliente.

Cuando el cliente se conecta, método accept() devuelve el objeto Socket que le pasaremos al constructor del hilo.

         socketClient = servidor.accept(); // ESPERE AL CLIENT
			FilServidor fil = new FilServidor(socketClient); // FIL ATENCION AL CLIENT
         fil.start(); // INICIE EL FIL

Todas las operaciones de atención al cliente se incluirán dentro de la clase hilo. A esto se le llama la lógica del servidor o la funcionalidad del servidor. En este caso transforma cadenas recibidas en mayúsculas hasta recibir "*"

El hilo principal del servidor recibe conexión, crea hilo de atención al cliente y se olvida del cliente.

************************************
LANZAR LA APP 
************************************

Esta aplicacion requiere tener java instalado

Iniciamos el servidor:
<pre>
javac Servidor.java 
java Servidor
</pre>

Iniciamos el cliente:
<pre>
javac Cliente.java
java Cliente
</pre>



                                                                                David M.
                                                                 11 de diciembre de 2023


