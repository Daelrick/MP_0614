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
   
    


   Si no hubiera conexión a internet, obtendríamos la siguiente respuesta

   ![Respuesta sin Internet](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/ksi3SF0nW4.jpg?raw=true)



### Opción 2

1. Ingresamos el comando **IPCONFIG**

2. Al ejecutar este comando se mostrará el adaptador activo que tengamos, indicándonos que estamos conectados a Internet

   ![Medios conectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/WGAVAu0MM4.jpg?raw=true)

3. Si no hubiera conexión a Internet, todos los medios se mostrarían desconectados

![Medios desconectados](https://github.com/Daelrick/MP_0614/blob/main/images/PowerShell/RxcFoxxJFv.jpg?raw=true)





##   ¿Cómo sabemos si nuestro servidor es accesible desde Internet? 

---









