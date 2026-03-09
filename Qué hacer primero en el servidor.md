¿Qué hacer primero en el servidor?
cat /etc/os-release mostrar la versión del sistema
uname -r muestra el kernel
uname -m muestra la arquitectura 
dpkg -l muestra los paquetes instalados
dpgk -l | grep "cups" muestra el servidor de impresión (librería libcups)
(cups utiliza el puerto 631 TCP)
(Recomendación de seguridad: dejar el servidor de impresión aislado, aparte de todos los demás servicios, en un solo hardware)
sudo apt install cups

systemctl list-units --type=service
sudo systemctl stop cups (si a este punto se reinicia, el servidor volverá a activarse)
sudo systemctl disable cups (si se reinicia, ya no se activará)

ps -aux mostrar los procesos y programas corriendo en el servidor. 

Los usuarios se localizan en /etc/passwd

grep /bin/bash /etc/passwd (los usuarios que pueden logearse a la terminal bash)

sudo adduser jacky (para agregar usuarios)

cat /etc/passwd (mostrar usuarios)

su jacky (cambiar a usuario jacky)

cat /etc/group (mostrar grupos)

sudo usermod -aG sudo jacky (dar permisos de sudo a jacky)

getent group sudo (mostrar quiénes tienen permisos de sudo)




