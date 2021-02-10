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

   *ping (sitio web)*

   ***Ejemplo:*** *ping www.institutotecnologico.telefonica.com*

2. Al ejecutar este comando serán enviados una serie de paquetes hacia el sitio web de destino y obtendremos respuesta de recibidos con los respectivos tiempos de envío.

   ![Respuesta con internet](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/54G1JjF8C7.jpg?raw=true)
   
    

3. Si no hubiera conexión a internet, obtendríamos la siguiente respuesta

   ![Respuesta sin Internet](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/ksi3SF0nW4.jpg?raw=true)



### Opción 2

1. Ingresamos el comando **IPCONFIG**

2. Al ejecutar este comando se mostrará el adaptador activo que tengamos, indicándonos que estamos conectados a Internet

   ![Medios conectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/WGAVAu0MM4.jpg?raw=true)

3. Si no hubiera conexión a Internet, todos los medios se mostrarían desconectados

![Medios desconectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/RxcFoxxJFv.jpg?raw=true)





##   ¿Cómo sabemos si nuestro servidor es accesible desde Internet? 

---





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







