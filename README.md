# Práctica 1.1 — Preparar el Servidor Base

## 1. Especificaciones del Servidor
* **Sistema Operativo:** Ubuntu Server 22.04 LTS
* **Nombre del Host:** serverander
* **Procesadores (CPU):** 2 vCPUs
* **Memoria RAM:** 2048 MB (2 GB)
* **Dirección IP:** 192.168.0.67
* **Usuario principal con sudo:** ander

## 2. Configuración de Red y Almacenamiento
* **Modo de Red:** Adaptador Puente (Bridge) en la interfaz `enp0s3` 
para asignación de IP en la red local y acceso SSH desde el host.
* **Disco:** 20 GB de almacenamiento virtualizado.

## 3. Actualización y Verificación del Sistema
* Se ha actualizado el índice de paquetes y el sistema mediante:
  `sudo apt update && sudo apt upgrade -y`
* Verificación de paquetes pendientes completada sin errores 
(`sudo apt list --upgradable`).
* Verificación de permisos del usuario `ander` en el grupo `sudo` 
realizada correctamente (`sudo whoami` -> `root`).

## 4. Acceso Remoto SSH sin Contraseña
* Se generó un par de claves SSH (Ed25519) en la máquina Host (Windows).
* Se copió la clave pública al archivo `~/.ssh/authorized_keys` del 
usuario `ander` en el servidor.
* Comprobada la conexión remota desde el Host mediante 
`ssh ander@192.168.0.67` sin requerir contraseña manual.

## 5. Instantáneas (Snapshots)
* **Snapshot de respaldo:** "Estado Inicial" creado tras la actualización
 completa y la configuración del acceso remoto SSH.
