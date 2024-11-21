# Manual de XAMPP

## Índice

- [Manual de XAMPP](#manual-de-xampp)
  - [Índice](#índice)
  - [Solución de problemas](#solución-de-problemas)
    - [Error al intentar inciar MYSQL en XAMPP](#error-al-intentar-inciar-mysql-en-xampp)

---

## Solución de problemas

### Error al intentar inciar MYSQL en XAMPP

Si al intentar iniciar MYSQL en XAMPP obtienes el siguiente error:

```
Attempting to start MySQL app...
 	Status change detected: running
 	Attempting to start Apache app...
 	Status change detected: running
 	Status change detected: stopped
 	Error: MySQL shutdown unexpectedly.
 	This may be due to a blocked port, missing dependencies, 
 	improper privileges, a crash, or a shutdown by another method.
 	Press the Logs button to view error logs and check
 	the Windows Event Viewer for more clues
 	If you need more help, copy and post this
 	entire log window on the forums

```

Esto puede deberse a que el servicio de MYSQL ha entrado en conflicto debido a problemas que tienen los archivos de configuración de XAMPP.

La solución a ejecutar es la siguiente:

1. Nos dirigimos al directorio de instalación de XAMPP, en mi caso es `C:\xampp\mysql\`
2. Cambiaremos el nombre de la carpeta `data` por `data_old`
3. Haremos una copia de la carpeta `backup` y la renombraremos `data`
4. Copiaremos todas carpetas de la carpeta `data_old` a la carpeta `data`(salvo las carpetas `mysql`, `performance_schema` y `phpmyadmin`)
5. Copiaremos el archivo `ibdata1` de la carpeta `data_old` a la carpeta `data`
6. A continuación podremos inciar el servicio de MYSQL

Ten en cuenta que esto es una medida temporal, por lo que se recomienda hacer una copia de seguridad de las bases de datos y reinstalar el servidor de XAMPP.