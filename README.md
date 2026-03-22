

# Dev
1. Clonar el repositorio
2. Crear un .env basado en el .env.template
3. Ejecutar el comando `git submodule update --init --recursive`, reconstruira los sub-modulos.
4. Ejecutar el comando `docker compose up --build`

# Pasos creación Git Submodules
1. Crear repositorio LAUNCHER en GITHUB
2. Clonar repositorio creado en maquina local.
3. Ejecutar comando, donde `<repository_url>` es URL del repositorio a clonar y, `<directory_name>` es la carpeta donde se guardara el proyecto (debe ser unico en el proyecto y tiene que ser el mismo que se definio en el docker-compose)
```
git submodule add <repository_url> <directory_name>
```

# Clonar repositorio desde la carpeta LAUNCHER (por primera vez)
1. Ejecutar comandi `git clone <ruta_repositorio_a_clonar>`
2. Ejecutar comando para inicializar
```
git submodule update --init --recursive
```
3. Ejecutar comando para actualizar referencia a sub-modulos
```
git submodule update --remote
```

# A tomar en cuenta
1. Al trabajar con el repositorio LAUNCHER que contiene los submodulos se debe tener en cuenta que primero se debe ACTUALIZAR y hacer PUSH en los submodulos modificados y, despues en el repositorio LAUNCHER o principal.
2. Si se ACTUALIZA o se realiza PUSH primero el repositorio LAUNCHER o principal se perderan las referencias de los submodulos modificados y es probable salten conflictos.