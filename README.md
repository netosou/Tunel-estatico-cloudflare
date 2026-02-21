# Implementación de tunel estatico cloudflare (windows)
Este proyecto detalla la creacion de un tunel estatico para la exposición segura de un servidor local de carga de archivos


##  Índice
2. [Requisitos Previos](#️requisitos-previos)
3. [Instalación del Servicio](#️instalación-del-servicio)
4. [Configuración del Hostname](#️configuración-del-hostname)
7. [Errores](#errores)


---

##  Requisitos Previos
* Servidor local corriendo en el puerto 3000.
* Permisos de Administrador en la terminal.
* Salida permitida a los puertos `443` (HTTPS) y `7844` (QUIC/Argo).
* Tener un dominio disponible.


---

##  Instalación del Servicio
### Paso 1: Configuración en el Dashboard de Cloudflare
1. Crear cuenta en [Dash de Cloudflare](https://dash.cloudflare.com/).
2. Navegue a **Networking > Tunnels > Create tunnel** y despues nombrar túnel.

![crear tunel](img/crear_tunel.png)
![crear tunel2](img/crear_tunel2.png)<br>

3. Nombrar tunel.

![Nombrar tunel](img/Nombrar_tunel.png)


4. Seleccionar el sistema operativo del servidor (windows 64 bit en este caso)
![Sistema operativo](img/Sistema_operativo.png)<br>
5. Descargar y correr el ejecuble con el link que te da la pagina(cloudflared-windows-amd64.msi en este caso)
6. Abrir la terminal como administrador y correr el comando que te genera la pagina
![Comando generado](img/Comando_generado.png)<br>
Despues de correr el comando de manera exitosa debera aparecer el siguiente mensaje:
![Tunnel_connected](img/Tunnel_connected.png)<br>

### Paso 2: Agregar dominio a cloudflare

## Errores
Error 1033
![Error1033](img/Error1033.png)<br>
Aparece cuando el servidor tiene un tunel corriendo diferente al que esta asignado al dominio
Solucion:
Correr el comando `cloudflared service uninstall y posteriormente correr el comamdo service install correspondiente
