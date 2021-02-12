## Acceder a PowerShell

---

Para realizar la actividad, en primer lugar debemos acceder a la consola PowerShell. Para ello realizaremos los siguientes pasos:

1. En la barra de tareas pulsamos el botón **Inicio**  

![Botón Inicio](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/JfOgWPMsL7.jpg?raw=true)


2. Seleccionamos la opción **todas las aplicaciones**

![Todas las aplicaciones](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/5SN6d0OKvm.jpg?raw=true)


3. Buscamos el directorio **Windows PowerShell** y lo desplegamos 

![Windows PowerShell](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/y6OUiCrDA0.jpg?raw=true)


4. Pulsamos botón derecho del ratón sobre **Windows PowerShell** y seleccionamos la opción **Ejecutar como administrador**

![pPJ8TvwdRh](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/pPJ8TvwdRh.jpg?raw=true)


5. Una vez pulsada la opción, se abrirá **PowerShell** en modo administrador.

![Consola PowerShell](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/n34s7me3hM.jpg?raw=true)

*Nota: si en la consola se muestra* ***system32***, *hemos ejecutado PowerShell como administrador*





## ¿Cómo sabemos si tenemos conexión a internet? 

------

### Opción 1

1. En la consola **PowerShell** escribimos la siguiente sintaxis y pulsamos Enter:

   ```powershell
   ping www.institutotecnologico.telefonica.com
   ```

   

2. Al ejecutar este comando serán enviados una serie de paquetes hacia el sitio web de destino y obtendremos respuesta de recibidos con los respectivos tiempos de envío.

   ![Respuesta con internet](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/54G1JjF8C7.jpg?raw=true)
   
    

3. Si no hubiera conexión a internet, obtendríamos la siguiente respuesta

   ![Respuesta sin Internet](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/ksi3SF0nW4.jpg?raw=true)



### Opción 2

1. Ingresamos el siguiente comando:

   ```powershell
   IPCONFIG
   ```

   

2. Al ejecutar este comando se mostrará el adaptador activo que tengamos, indicándonos que estamos conectados a Internet

   ![Medios conectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/WGAVAu0MM4.jpg?raw=true)

3. Si no hubiera conexión a Internet, todos los medios se mostrarían desconectados

![Medios desconectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/RxcFoxxJFv.jpg?raw=true)





##   ¿Cómo sabemos si nuestro servidor es accesible desde Internet? 

---

Este comando es una herramienta para poder determinar nuestras conexiones tanto internas (localhost) como externas.

En este caso usaremos la siguiente sintaxis

```powershell
netstat -ano
```

*Nos mostraría* ***todas*** *las conexiones  en formato numérico y agregaría el número de ID del proceso que está ejecutándose en ese puerto*

![Respuesta](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/JGlaPlVVws.jpg?raw=true)



- **Proto**: protocolo establecido para establecer la comunicación. Aquí fundamentalmente veremos tres tipos de protocolos: ICMP, UDP y TCP

- **Dirección Local**: aquí nos aparece el número de IP local que establece una comunicación de salida

- **Dirección remota**: vemos la dirección IP remota a la que estamos conectados, y vemos también que aparece la dirección correspondiente a localhost, es decir a nuestro propio equipo

- **Estado**: nos indica en que estado se encuentra la comunicación entre procesos, y veremos diferentes tipos

*LISTENING,* o escuchando, significa que detrás de ese puerto hay un proceso esperando que alguien hable con él, es decir, en disposición de aceptar comunicaciones. 

*ESTABLISHED,* o establecidas, significa que el proceso que está detrás de ese puerto ya está hablando con algo o alguien; la columna de dirección remota nos indica con quién habla. 

*SYN_SEND*, indica una solicitud de comunicación por nuestra parte, es decir, es como si estuviéramos llamando a alguien y esperando a que nos respondiera.

*SYN_RECEIVED*, indica que el servidor remoto ha aceptado nuestra solicitud de comunicación. Al que estábamos llamando por móvil ya nos ha descolgado, pero todavía no nos ha dicho nada.

*FIN_WAIT_1*, indica que hemos solicitado terminar la comunicación. A nuestro amigo el del móvil, le hemos dicho que vamos a colgar.

*FIN_WAIT_2,* no es muy habitual ver este estado en nuestra comunicaciones, entramos en él cuando hemos solicitado terminar la comunicación pero el servidor no se da por enterado.

*TIMED_WAIT*, estamos esperando a que el servidor acepte nuestra petición de cerrar comunicación. Nuestro amigo el del móvil, nos ha dicho que nos esperemos un momento antes de colgar.

*CLOSE_WAIT*, indica una solicitud de cierre pasiva entre cliente y servidor. Siguiendo con nuestro amigo el del móvil, digamos que aceptamos esperar hasta terminar la comunicación y le decimos que la cierre él cuando quiera, que nosotros dejamos el móvil encendido y nos vamos a hacer otras cosas.

*LAST_ACK,* aquí es nuestro amigo el del móvil el que nos dice que nos cuelga, es decir es el servidor el que nos dice que va a cerrar la comunicación.

*CLOSED*, comunicación entre cliente y servidor cerrada.



## ¿Cómo sabemos a quién pertenece una dirección web (URL)?

---

**nslookup** es una herramienta de línea de comandos, cuya función básica es encontrar la dirección IP de un equipo determinado o realizar una búsqueda DNS inversa (es decir, encontrar el nombre de dominio de una determinada dirección IP).

Para usar el comando, en este caso preguntamos quien es ***es.wikipedia.org***

```powershell
nslookup es.wikipedia.org
```

![Quien es](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/nGrV77ywtW.jpg?raw=true)

Ahora podemos preguntarle quien es ***2620:0:862:ed1a::1***

```powershell
nslookup 2620:0:862:ed1a::1
```

![Quien es](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/CYjJDxUmgM.jpg?raw=true)

Vemos que aparecen diferentes datos en ambas respuestas

- **Servidor**: nos indica el nombre del servidor DNS que va a utilizar la herramienta para realizar las consultas.
- **Address**: la dirección IP del DNS que estamos utilizando.
- **Respuesta no autoritativa**: la respuesta DNS se ha producido desde un servidor DNS que tiene en caché una copia de las consultas realizadas
- **Nombre**: indica el nombre del dominio que estamos buscando
- **Address**: las direcciones que corresponden a ese dominio.



## ¿Cómo probamos que podemos acceder a un servidor? 

---

El comando **Curl** está diseñado para funcionar como una forma de verificar la conectividad a las URL y como una gran herramienta para transferir datos.

Podemos verificar que la solicitud que realizamos tiene éxito ***(código de respuesta de estado satisfactorio HTTP 200 OK)***

### Opción 1

Para ello podemos tener una URL de una imagen de Github y realizar la siguiente sintaxis:

```powershell
curl https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/pPJ8TvwdRh.jpg?raw=true
```

Si pulsamos ***ENTER*** deberemos obtener una respuesta 200 y quiere decir que alcanzamos al servidor

![Statuscode 200](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/Tfsrtpk9xJ.jpg?raw=true)

### Opción 2

Por otro lado, también podemos descargar la imagen indicada anteriormente para ver si tenemos acceso al servidor. Podemos hacerlo de la siguiente forma:

```powershell
curl https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/pPJ8TvwdRh.jpg?raw=true -o prueba_descarga.jpg
```

Si pulsamos ***ENTER*** la imagen se descargará en el directorio en el que nos encontremos

![Descarga de imagen](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/eFZJT9dleR.jpg?raw=true)



