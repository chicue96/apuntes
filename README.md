# apuntes
Apuntes utiles de programacion

GENERAR LLAVE SSH para GITHUB
>ssh-keygen -t ed25519 -C tu_correo@example.com
//-t ed25519 establece el nivel de encriptación.
//-C añade un comentario con tu correo, útil para identificar la llave en GitHub.

**Guardar y proteger la llave:
**Usa el nombre por defecto y añade una contraseña segura.
**La llave pública se guarda en el directorio .ssh, generalmente nombrada id_ed25519.pub.
**Configurar el agente SSH: Activa el agente de SSH y añade la llave privada:

>eval "$(ssh-agent -s)"
>ssh-add ~/.ssh/id_ed25519
**¿Cómo añadir la llave SSH a GitHub?
Abrir el archivo de la llave pública (id_ed25519.pub) y copia el contenido.
En GitHub, ve a Settings > SSH and GPG keys > New SSH key y pega la llave.
Nombra la llave de acuerdo a la computadora en la que estás configurándola.