administración de servidor

systemctl list-units --type=service

CHMOD funciona con 3 espacios de 3 bits. Cada bit reprsenta un permiso

100 leer
010 escribir
001 ejecutar (necesario para los scripts)

CHMOD XYZ

X = permisos de usuario
Y = permisos de grupo
Z = permisos de otros


scripts para monitorear servicios
ssh
ftp
apache2
fail2ban
firewall ufw
isc-dhcp

script

```
#!/bin/bash
 
# Menù para el usuario
while true
do
echo "Validar servicios"
echo "1.- Ver estado de un Servicio"
echo "2.- Iniciar servicio"
echo "3.- Detener servicio"
echo "4.- Reiniciar servicio"
echo "5.- Salir"
 
# Leer un input de un usuario -p sirve para imprimir un mensaje para la entrada
read -p "Selecciona una opcion" opcion
# tambièn aquì podemos poner la linea de read -p para que su alcance sea global para
# el switch case
 
 
# invocas  variables con un signo '$' antes de cada variable, de m anera que: $variable
case $opcion in
1) read -p "Nombre del servicio" servicio
   systemctl status $servicio ;;
# paramos esta clàusula con ;;
 
2) read -p "Nombre del servicio" servicio
   sudo systemctl start $servicio ;;
 
3) read -p "Nombre del servicio" servicio
   sudo systemctl stop $servicio  ;;
 
4) read -p "Nombre del servicio" servicio
   sudo systemctl restart $servicio ;;
 
5) echo "Aqui se rompio una taza y cada quien a su casa..."
break
;;
# no confundir el break de arriba con el del switch case. El Switch case todavìa sigue abierto
*) echo "Ay carlitosSSS..."
;;
# el operador * nos dice que cualquier otro caracter, serà invàlido
esac
#con esac rompemos el case, lo detenmos.
 
done
# done detenemos el bucle. Piensa en inglès "while do" pasado de do? "done"
```
