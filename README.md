# Implementación de tunel estatico cloudflare (windows)
Este proyecto detalla la creacion de un tunel estatico para la exposición segura de un servidor local de carga de archivos


## 📑 Índice
1. [🏗️ Arquitectura del Sistema](#-arquitectura-del-sistema)
2. [📋 Requisitos Previos](#-requisitos-previos)
3. [🛠️ Instalación del Servicio](#️-instalación-del-servicio)
4. [⚙️ Configuración del Hostname](#️-configuración-del-hostname)
5. [⚠️ Especificaciones y Límites](#️-especificaciones-y-límites)
6. [🧪 Verificación de Conectividad](#-verificación-de-conectividad)
7. [🆘 Solución de Problemas (Troubleshooting)](#-solución-de-problemas-troubleshooting)

---

## 🏗️ Arquitectura del Sistema
*(Aquí va tu diagrama o descripción del flujo de datos)*

---

## 📋 Requisitos Previos
* Servidor local corriendo en el puerto XXXX.
* Permisos de Administrador en la terminal.
* Salida permitida al puerto **7844 (QUIC)**.

---

## 🛠️ Instalación del Servicio
Para instalar el conector permanente en Windows:
```powershell
cloudflared service install <TU_TOKEN>
Start-Service Cloudflared
