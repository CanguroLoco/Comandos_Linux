# Comandos_Linux
comandos extraídos de una clase de linux en servidores. 

| Programa | Función Corta |
| --- | --- |
| net-tools | Conjunto de herramientas clásicas para controlar redes (incluye ifconfig, netstat y route). |
| traceroute | Rastrea la ruta que siguen los paquetes desde tu equipo hasta un host destino. |
| arp-scan | Escanea la red local enviando paquetes ARP para identificar dispositivos conectados. |
| hydra | Herramienta de auditoría de seguridad para realizar ataques de fuerza bruta contra protocolos de red. |

| Comando Base | Opciones / Argumentos | Archivo, Directorio o Target |
| --- | --- | --- |
| git | clone | https://github.com/bitbrute/evillimiter.git, https://github.com/NguyenLTVinh/tuxsay.git |
| evillimiter | scan, --range, -h, -g, hosts, --no-unicode, -v, --version | 10.1.213.1, 10.1.213.255, GATEWAY_IP |
| python3 | (Ninguna) | setup.py, tuxsay.c |
| which | (Ninguna) | evillimiter |
| locale | (Ninguna) | (Configuración de sistema) |
| locale-gen | (Ninguna) | en_US.UTF-8 |
| update-locale | LANG= | en_US.UTF-8 |
| export | (Ninguna) | LANG, TERM |
| echo | (Ninguna) | `"  |
| rm  | -R, -rf | /etc, ~/tuxsay |
| mkdir | (Ninguna) | Descargas |
| wget | (Ninguna) | (URLs de SourceForge) |
| sl  | (Ninguna) | (Animación) |
| asciiquarium | (Ninguna) | (Animación) |
| ponysay | (Ninguna) | "maqueavelico", "hola", "submaskara" |
| toilet | (Ninguna) | "ir51m", "Hola", "hi" |
| neofetch | (Ninguna) | (Información de sistema) |
| snap | install | neotyfetch, tuxfishing, asciiquarium, ponysay |
| figlet | (Ninguna) | "cowsay", "hi" |
| lolcat | (Ninguna) | "whasa", "hi" |
| fortune | (Ninguna) | (Salida aleatoria) |
| pipes.sh | -p, -t | (Animación) |
| pip / pipx | install, ensurepath | tuxsay |
| make | install | (Directorio actual) |
| reboot | (Ninguna) | (Sistema) |
| freedoom | (Ninguna) | (Juego) |
| traceroute | (Ninguna) | 8.8.8.8, 148.229.1.1 |
| arp-scan | --localnet, --ens18 | (Red local) |
| shutdown | (Ninguna) | (Sistema) |


| Comando Base | Nuevas Opciones / Argumentos | Archivo o Directorio Adicional |
| --- | --- | --- |
| apt | upgrade, list --upgradable | net-tools, hydra, build-essential, python3-pip, pipx, traceroute |
| systemctl | enable --now, reload | ssh, vsftpd |
| ip  | route, link, neigh flush all, neighbor flush all | (Configuración de red) |
| grep | -r, -rl, -oE | /etc/, access.log, filename.txt |
| nmap | -sU, -p, --script, -sS, -Pn, -T5, -p- | dns-brute, 10.60.137.104, 10.60.137.30 |
| awk | $3 == 404 {print $1,$3}' | access.log, error.log |
| tail | -f  | error.log |
| cd  | (Rutas nuevas) | evillimiter, Descargas, /var/log/apache2, tuxsay |


| Comando Base | Opciones / Argumentos | Filtro / Contexto |
| --- | --- | --- |
| grep | -i  | "ssh", "sudo", "failed", "Failed password", "firewall", "sessions", "error", "memory", "ens18", "fail login", "FAIL LOGIN" |
| awk | -F  | (Procesamiento de columnas en vsftpd.log e ip a) |
| tree | (Ninguna) | (Directorio actual) |
| cowsay | -t  | "hi", "67", "vhoylavv" |
| date | --set= | "2026-02-19 8:25:30" |
| man | (Ninguna) | cowsay, grep, tail, systemctl, journalctl, awk |
| sort | (Ninguna) | (Salida de pipe) |
| uniq | -c  | (Salida de pipe) |
| who | am i | (Usuarios) |
| whoami | (Ninguna) | (Usuario actual) |
| last / lastb | (Ninguna) | (Registros de login) |
| ps  | -aux | (Procesos) |
| curl | (Ninguna) | http://10.1.213.70, http://10.1.213.50 |


| Comando Base | Opciones / Argumentos | Objetivo (IP / Interfaz / Servicio) |
| --- | --- | --- |
| apt | install, update, -y | tree, apache2, cowsay, openssh-server, vsftpd, isc-dhcp-server, logrotate, cmatrix, nmap |
| systemctl | status, stop, restart | apache2, ssh, sshd, vsftpd, isc-dhcp-server |
| ip  | address, a, -4 a, route, neigh, add show dev | ens18 |
| ss  | -tulnp, -ant, -tuln | (Red/Puertos) |
| nmap | -sV, -O | 10.1.213.50, 10.1.213.68, 10.1.213.70, 10.1.213.51 |
| ping | (Ninguna) | 10.1.213.6, 10.1.213.69 |
| tcpdump | -i  | ens18 arp, ens18 tcp |
| netplan | apply | (Configuración de red) |
| hostname | (Ninguna) | (Sistema) |
| journalctl | -u  | sshd.service, sshd, ssh |

| Comando Base | Opciones / Argumentos | Archivo o Directorio |
| --- | --- | --- |
| nano | (Ninguna) | juan.txt, /etc/netplan/50-cloud-init.yaml, index.html, vsftpd.conf, /etc/dhcp/dhcpd.conf, dhcpd.conf, hola.txt |
| cd  | (Ninguna) | ~, .., /etc/apache2/, /var/www, html, /etc/, ssh, /etc/dhcp, /var/log, /etc/logcheck, logrotate.d, apache2 |
| ls  | -l, - | /etc/passwd, /etc/, /var/log |
| pwd | (Ninguna) | (Directorio actual) |
| cp  | (Ninguna) | dhcpd.conf, dhcpd.conf.respaldo |
| cat | (Ninguna) | /etc/passwd, /etc/shadow, auth.log, /etc/logrotate.conf, vsftpd.log, log, kern.log, access.log |
| tail | -f  | /var/log/syslog, /var/log/auth.log, /var/log/kern.log |
| du  | -sh | /var/log |

