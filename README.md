# Implementación de tunel estatico cloudflare (windows)
Este proyecto detalla la creacion de un tunel estatico para la exposición segura de un servidor local de carga de archivos


##  Índice
2. [Requisitos Previos](#️requisitos-previos)
3. [Instalación del Servicio](#️instalación-del-servicio)
4. [Configuración del Hostname](#️configuración-del-hostname)
7. [Solución de Problemas (Troubleshooting)](#solución-de-problemas-troubleshooting)


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

4. En **Public Hostname**, configure su dominio/subdominio apuntando al servicio local:


## Solución de Problemas (Troubleshooting)
