# Lista de comandos de git muy útiles

- `~$: git init` Para que git comience a monitorizar lo que pasa en el directorio.
- `~$: git commit -m "mensaje"` Para que git cree un commit con el mensaje `"mensaje"`.
- `~$: git push origin master` Para que git suba al repositorio remoto los cambios que has hecho.
- `~$: git add archivo` Para que git reconozca que estás haciendo coas con ese archivo, y siga los cambios. Sino no podrás hacer un commit.

__Nota: para que estos cambios sirvan de algo en GitHub, hay que tener conectados los dos repos__

Para conectar dos repos:

1.`~$: ssh-keygen -t rsa -C "correo_de_git@dominio.com"`. Esto genera una clave rsa en `~/.ssh/`
2.  Copia la clave pública (`id_rsa.pub`) y métela en tu cuenta de GitHub: Settings -> SSH and GPG keys. Una vez que la tengas ya puedes dedicarte a hacer cosas en tu pc y subirlas luego a GitHub sin problemas!

## Comandos poderosos...

- `~$: git push --force --set-upstream origin master` Para forzar la sincronización del repo remoto con tu repo local. Útil para revertir cambios. **MANEJAR CON CUIDADO**.
