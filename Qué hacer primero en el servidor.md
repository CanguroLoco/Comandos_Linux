Aquí tienes una versión mejorada y organizada del documento en formato Markdown, con una estructura más clara y bloques de código para facilitar su lectura:

# Guía: ¿Qué hacer primero en el servidor?

Esta guía detalla los comandos básicos para la inspección inicial, gestión de servicios (CUPS) y administración de usuarios en un sistema basado en Linux.

## 1. Información del Sistema
Para conocer el entorno en el que estamos trabajando:

*   **Versión del sistema:** `cat /etc/os-release`
*   **Versión del Kernel:** `uname -r`
*   **Arquitectura del hardware:** `uname -m`

## 2. Gestión de Paquetes y Servicios
### Listado de paquetes
*   **Mostrar todos los paquetes instalados:** `dpkg -l`
*   **Buscar un paquete específico (ej. CUPS):** `dpkg -l | grep "cups"`

### Servidor de Impresión (CUPS)
> **Nota de seguridad:** Se recomienda dejar el servidor de impresión aislado de los demás servicios en un hardware independiente. Utiliza el puerto **631 TCP**.

*   **Instalación:**
    ```bash
    sudo apt install cups
    ```
*   **Listar servicios activos:**
    ```bash
    systemctl list-units --type=service
    ```
*   **Detener el servicio (temporal):**
    ```bash
    sudo systemctl stop cups
    ```
*   **Deshabilitar el inicio automático:**
    ```bash
    sudo systemctl disable cups
    ```

## 3. Procesos y Usuarios
### Monitoreo
*   **Mostrar procesos y programas en ejecución:** `ps -aux`

### Gestión de Usuarios
Los usuarios se localizan en el archivo `/etc/passwd`.

*   **Filtrar usuarios con acceso a terminal Bash:**
    ```bash
    grep /bin/bash /etc/passwd
    ```
*   **Crear un nuevo usuario:**
    ```bash
    sudo adduser jacky
    ```
*   **Listar todos los usuarios:**
    ```bash
    cat /etc/passwd
    ```
*   **Cambiar al usuario creado:**
    ```bash
    su jacky
    ```

### Grupos y Permisos
*   **Mostrar grupos existentes:**
    ```bash
    cat /etc/group
    ```
*   **Dar permisos de sudo a un usuario:**
    ```bash
    sudo usermod -aG sudo jacky
    ```
*   **Verificar quiénes tienen permisos de sudo:**
    ```bash
    getent group sudo
    ```

filtrar quiénes tienen acceso a bash y permisos
grep /bin/bash /etc/passwd

en /etc/fail2ban/jail.conf 

tail -f archivo para monitorear logs en tiempo real

ss -tunap para ver las conexiones establecidas 

sudo apt install chkrootkit para escanear virus?

sudo chkrootkit para correr el antivirus

grep "Accepted" /var/log/auth para filtrar conexiones exitosas de ssh

arp who-has 10.1.213.50 tell 10.1.213.70 para descubrir la MAC de esa ip (no sirvió xd)

nmap 10.1.213.89
