# Implementación de tunel estatico cloudflare (windows)
Este proyecto detalla la creacion de un tunel estatico para la exposición segura de un servidor local de carga de archivos


## 📑 Índice
2. [📋 Requisitos Previos](#-requisitos-previos)
3. [🛠️ Instalación del Servicio](#️-instalación-del-servicio)
4. [⚙️ Configuración del Hostname](#️-configuración-del-hostname)
5. [⚠️ Especificaciones y Límites](#️-especificaciones-y-límites)
6. [🧪 Verificación de Conectividad](#-verificación-de-conectividad)
7. [🆘 Solución de Problemas (Troubleshooting)](#-solución-de-problemas-troubleshooting)


---

## 📋 Requisitos Previos
* Servidor local corriendo en el puerto 3000.
* Permisos de Administrador en la terminal.
* Salida permitida a los puertos `443` (HTTPS) y `7844` (QUIC/Argo).

---

## 🛠️ Instalación del Servicio
Para instalar el conector permanente en Windows:
```powershell
cloudflared service install <TU_TOKEN>
Start-Service Cloudflared
