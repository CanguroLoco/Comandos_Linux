# Comandos_Linux
comandos extraídos de una clase de linux en servidores. 

Aquí tienes las tablas actualizadas con las dos columnas adicionales ("Función del Comando" y "Explicación de Argumentos") para detallar qué hace cada herramienta y para qué sirven las opciones especificadas:

```markdown
# Comandos_Linux
comandos extraídos de una clase de linux en servidores. 

| Programa | Función Corta |
| --- | --- |
| net-tools | Conjunto de herramientas clásicas para controlar redes (incluye ifconfig, netstat y route). |
| traceroute | Rastrea la ruta que siguen los paquetes desde tu equipo hasta un host destino. |
| arp-scan | Escanea la red local enviando paquetes ARP para identificar dispositivos conectados. |
| hydra | Herramienta de auditoría de seguridad para realizar ataques de fuerza bruta contra protocolos de red. |

### Herramientas y Utilidades Generales

| Comando Base | Opciones / Argumentos | Archivo, Directorio o Target | Función del Comando | Explicación de Argumentos |
| --- | --- | --- | --- | --- |
| git | clone | https://github.com/... | Sistema de control de versiones. | `clone`: Descarga una copia exacta de un repositorio remoto. |
| evillimiter | scan, --range, -h, -g, hosts, --no-unicode, -v, --version | 10.1.213.1, 10.1.213.255, GATEWAY_IP | Limita el ancho de banda de dispositivos en la red local. | `scan`: Busca dispositivos. `--range`: Define rango de IPs. `-h`: Ayuda. `-g`: Gateway. `--no-unicode`: Texto simple. `-v / --version`: Muestra versión. |
| python3 | (Ninguna) | setup.py, tuxsay.c | Intérprete del lenguaje de programación Python. | (Sin argumentos extra, ejecuta el script o inicia la consola). |
| which | (Ninguna) | evillimiter | Muestra la ruta completa del ejecutable de un comando. | (Solo recibe el nombre del programa a buscar). |
| locale | (Ninguna) | (Configuración de sistema) | Muestra información sobre la configuración regional y el idioma. | (Muestra las variables actuales de entorno). |
| locale-gen | (Ninguna) | en_US.UTF-8 | Genera los archivos de configuración regional especificados. | (Recibe el idioma a generar, ej: Inglés UTF-8). |
| update-locale | LANG= | en_US.UTF-8 | Actualiza la configuración regional predeterminada del sistema. | `LANG=`: Define la variable de idioma del sistema. |
| export | (Ninguna) | LANG, TERM | Define variables de entorno para la sesión actual. | (Recibe la variable y su valor a exportar). |
| echo | (Ninguna) | `" | Imprime texto o variables en la terminal. | (Imprime la cadena de texto proporcionada). |
| rm  | -R, -rf | /etc, ~/tuxsay | Elimina archivos o directorios. | `-R / -r`: Recursivo (directorios). `-f`: Forzar (sin preguntar). |
| mkdir | (Ninguna) | Descargas | Crea nuevos directorios. | (Recibe el nombre del directorio a crear). |
| wget | (Ninguna) | (URLs de SourceForge) | Descarga archivos desde internet (HTTP, HTTPS, FTP). | (Recibe la URL del archivo a descargar). |
| sl  | (Ninguna) | (Animación) | Broma de terminal (muestra un tren cuando escribes mal 'ls'). | (Ninguna) |
| asciiquarium | (Ninguna) | (Animación) | Muestra un acuario animado en arte ASCII. | (Ninguna) |
| ponysay | (Ninguna) | "maqueavelico", "hola", "submaskara" | Muestra un pony en ASCII diciendo el texto ingresado. | (Recibe el mensaje a mostrar). |
| toilet | (Ninguna) | "ir51m", "Hola", "hi" | Genera texto grande en arte ASCII con caracteres coloridos. | (Recibe el texto a transformar). |
| neofetch | (Ninguna) | (Información de sistema) | Muestra información del sistema y hardware de forma visual. | (Ninguna) |
| snap | install | neotyfetch, tuxfishing... | Gestor de paquetes universales para Linux. | `install`: Descarga e instala el paquete especificado. |
| figlet | (Ninguna) | "cowsay", "hi" | Genera texto grande en arte ASCII (similar a toilet). | (Recibe el texto a transformar). |
| lolcat | (Ninguna) | "whasa", "hi" | Añade colores del arcoíris a la salida de texto en terminal. | (Recibe texto o procesa la salida de otro comando). |
| fortune | (Ninguna) | (Salida aleatoria) | Muestra una frase o cita aleatoria. | (Ninguna) |
| pipes.sh | -p, -t | (Animación) | Muestra tuberías animadas en la terminal. | `-p`: Número de tuberías. `-t`: Tipo de caracteres a usar. |
| pip / pipx | install, ensurepath | tuxsay | Gestor de paquetes de Python. | `install`: Instala paquetes. `ensurepath`: Añade pipx a la variable PATH. |
| make | install | (Directorio actual) | Herramienta de compilación y automatización. | `install`: Ejecuta la regla de instalación del Makefile. |
| reboot | (Ninguna) | (Sistema) | Reinicia el sistema operativo. | (Ninguna) |
| freedoom | (Ninguna) | (Juego) | Clon de código abierto del juego Doom. | (Ninguna) |
| traceroute | (Ninguna) | 8.8.8.8, 148.229.1.1 | Rastrea la ruta de paquetes hacia un destino. | (Recibe la IP o dominio destino). |
| arp-scan | --localnet, --ens18 | (Red local) | Escáner de red basado en el protocolo ARP. | `--localnet`: Escanea toda la subred local. `--ens18`: Especifica la interfaz de red. |
| shutdown | (Ninguna) | (Sistema) | Apaga el sistema operativo. | (Ninguna) |

### Gestión del Sistema y Redes

| Comando Base | Nuevas Opciones / Argumentos | Archivo o Directorio Adicional | Función del Comando | Explicación de Argumentos |
| --- | --- | --- | --- | --- |
| apt | upgrade, list --upgradable | net-tools, hydra... | Gestor de paquetes para Debian/Ubuntu. | `upgrade`: Actualiza paquetes. `list --upgradable`: Muestra qué se puede actualizar. |
| systemctl | enable --now, reload | ssh, vsftpd | Administra los servicios del sistema (systemd). | `enable --now`: Habilita al arranque e inicia ya. `reload`: Recarga configuración sin apagar. |
| ip  | route, link, neigh flush all, neighbor flush all | (Configuración de red) | Muestra o manipula enrutamiento, interfaces y túneles. | `route`: Muestra rutas. `link`: Interfaces. `neigh flush all`: Limpia la caché ARP. |
| grep | -r, -rl, -oE | /etc/, access.log, filename.txt | Busca patrones de texto dentro de archivos o salidas. | `-r`: Búsqueda recursiva. `-l`: Solo nombres de archivo. `-o`: Solo coincidencias. `-E`: Expresiones regulares extendidas. |
| nmap | -sU, -p, --script, -sS, -Pn, -T5, -p- | dns-brute, 10.60.137... | Herramienta de exploración de red y auditoría de seguridad. | `-sU`: Escaneo UDP. `-p`: Puertos. `--script`: Ejecuta scripts (ej: dns-brute). `-sS`: Escaneo SYN (sigiloso). `-Pn`: Evita el ping previo. `-T5`: Velocidad máxima (agresivo). `-p-`: Escanea todos los 65535 puertos. |
| awk | $3 == 404 {print $1,$3}' | access.log, error.log | Lenguaje de procesamiento y escaneo de patrones en texto. | `$3 == 404`: Filtra si la 3ra columna es 404. `{print...}`: Imprime las columnas 1 y 3. |
| tail | -f  | error.log | Muestra la última parte (cola) de un archivo. | `-f`: (Follow) Muestra los cambios en el archivo en tiempo real. |
| cd  | (Rutas nuevas) | evillimiter, Descargas... | Cambia de directorio de trabajo. | (Recibe la ruta hacia donde navegar). |

### Filtros y Contextos

| Comando Base | Opciones / Argumentos | Filtro / Contexto | Función del Comando | Explicación de Argumentos |
| --- | --- | --- | --- | --- |
| grep | -i  | "ssh", "sudo", "failed"... | Busca patrones de texto. | `-i`: Ignora mayúsculas y minúsculas en la búsqueda. |
| awk | -F  | (Procesamiento de columnas) | Procesamiento de texto estructurado. | `-F`: Define un separador de campos personalizado (ej: comas o dos puntos). |
| tree | (Ninguna) | (Directorio actual) | Muestra el contenido de directorios en formato de árbol. | (Ninguna) |
| cowsay | -t  | "hi", "67", "vhoylavv" | Dibuja una vaca ASCII que dice el texto indicado. | `-t`: (dependiendo de la versión, pero usualmente para modo texto/estilo visual o es un error tipográfico por otro parámetro como -f). |
| date | --set= | "2026-02-19 8:25:30" | Muestra o configura la fecha y hora del sistema. | `--set=`: Establece manualmente la fecha y hora. |
| man | (Ninguna) | cowsay, grep, tail... | Muestra el manual oficial (documentación) de un comando. | (Recibe el nombre del comando a consultar). |
| sort | (Ninguna) | (Salida de pipe) | Ordena líneas de archivos de texto o salidas de comandos. | (Ninguna, ordena alfanuméricamente por defecto). |
| uniq | -c  | (Salida de pipe) | Filtra o reporta líneas repetidas adyacentes. | `-c`: Cuenta cuántas veces se repite cada línea. |
| who | am i | (Usuarios) | Muestra quién está conectado al sistema. | `am i`: Muestra solo la información de la sesión actual del usuario. |
| whoami | (Ninguna) | (Usuario actual) | Imprime el nombre del usuario efectivo actual. | (Ninguna) |
| last / lastb | (Ninguna) | (Registros de login) | Muestra un listado de los últimos usuarios conectados / intentos fallidos. | (Ninguna) |
| ps  | -aux | (Procesos) | Reporta el estado actual de los procesos del sistema. | `-a`: Todos los usuarios. `-u`: Formato orientado a usuario. `-x`: Procesos sin terminal asociada. |
| curl | (Ninguna) | http://10.1.213.70... | Transfiere datos desde o hacia un servidor (HTTP/FTP...). | (Recibe la URL a la cual hacer la petición web). |

### Configuración de Objetivos y Servicios

| Comando Base | Opciones / Argumentos | Objetivo (IP / Interfaz / Servicio) | Función del Comando | Explicación de Argumentos |
| --- | --- | --- | --- | --- |
| apt | install, update, -y | apache2, openssh-server... | Gestor de paquetes (Debian/Ubuntu). | `install`: Instalar. `update`: Actualizar repositorios. `-y`: Asumir "sí" a todas las preguntas. |
| systemctl | status, stop, restart | apache2, ssh, sshd... | Administra los servicios de systemd. | `status`: Muestra estado. `stop`: Detiene servicio. `restart`: Reinicia servicio. |
| ip  | address, a, -4 a, route... | ens18 | Herramienta de red (reemplaza ifconfig). | `address / a`: Direcciones IP. `-4`: Solo IPv4. `add show dev`: Mostrar detalles de dispositivo. |
| ss  | -tulnp, -ant, -tuln | (Red/Puertos) | Investiga sockets (puertos abiertos y conexiones, reemplaza netstat). | `-t`: TCP. `-u`: UDP. `-l`: En escucha. `-n`: Puertos numéricos. `-p`: Muestra el proceso. `-a`: Todos. |
| nmap | -sV, -O | 10.1.213.50... | Escáner de red. | `-sV`: Detecta versiones de servicios. `-O`: Detecta Sistema Operativo. |
| ping | (Ninguna) | 10.1.213.6... | Envía paquetes ICMP ECHO_REQUEST a hosts de red para verificar conectividad. | (Recibe la IP o dominio objetivo). |
| tcpdump | -i  | ens18 arp, ens18 tcp | Analizador de paquetes de red desde la consola (Sniffer). | `-i`: Especifica la interfaz a escuchar (ej: ens18). |
| netplan | apply | (Configuración de red) | Utilidad para configurar redes en Ubuntu/Debian modernos. | `apply`: Aplica los cambios realizados en los archivos .yaml de configuración. |
| hostname | (Ninguna) | (Sistema) | Muestra o establece el nombre de red del sistema. | (Ninguna, para mostrar el nombre actual). |
| journalctl | -u  | sshd.service, sshd, ssh | Consulta los registros (logs) recogidos por systemd. | `-u`: Filtra los logs por la unidad/servicio específico. |

### Navegación y Archivos

| Comando Base | Opciones / Argumentos | Archivo o Directorio | Función del Comando | Explicación de Argumentos |
| --- | --- | --- | --- | --- |
| nano | (Ninguna) | juan.txt, /etc/netplan/... | Editor de texto en terminal fácil de usar. | (Recibe la ruta o nombre del archivo a editar/crear). |
| cd  | (Ninguna) | ~, .., /etc/apache2/... | Cambia de directorio de trabajo. | `~`: Home. `..`: Sube un nivel. |
| ls  | -l, - | /etc/passwd, /etc/... | Lista el contenido de un directorio. | `-l`: Formato de lista larga (permisos, dueño, tamaño, fecha). |
| pwd | (Ninguna) | (Directorio actual) | Imprime el nombre del directorio de trabajo actual (Print Working Directory). | (Ninguna) |
| cp  | (Ninguna) | dhcpd.conf, dhcpd.conf.respaldo | Copia archivos o directorios. | (Recibe archivo origen y nombre/ruta destino). |
| cat | (Ninguna) | /etc/passwd, /etc/shadow... | Concatena archivos e imprime el contenido en la salida estándar (terminal). | (Recibe el archivo que se desea leer). |
| tail | -f  | /var/log/syslog... | Muestra la parte final de los archivos. | `-f`: Sigue los cambios del archivo en vivo. |
| du  | -sh | /var/log | Muestra el uso de espacio en disco de archivos y directorios. | `-s`: Resumen (Total). `-h`: Formato legible para humanos (MB, GB). |
```
