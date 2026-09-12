
# Laboratorio 02

Hoy se utilizara docker compose para poder desplegar un trabajo, servicio web y una base de datos

## Stack
API
- Minimal API
- Debe retornar un mensaje incluyendo mi nombre
- Docker
- docker run -d --rm -p 3000:3000 nmatsui/hello-world-api. 8c446d43dfc9
focused_wilson
docker run -d --rm -p 3001:3000 nmatsui/hello-world-api sweet_sammet
BD
- PostgreSQL
- $ docker run --name some-postgres -e POSTGRES_PASSWORD=example -d
postgres

## Tipos de redes en Docker

- Puente: Controlador por defecto cuando levantas un contenedor independiente
- Host: El contenedor se conecta directamente al host
- Overlay: Permite la comunicación entre contenedores que están en diferentes host
- Macvlan: Permite que los contenedores tengan su propia dirección IP en la red

## Tipos de volumenes en Docker

- Volúmenes con nombre: Mecanismo recomendado para persistir datos generados por y para contenedores.
- Montajes vinculados: Tienen acceso directo al sistema de archivos local
-Montajes en memoria: Los datos solo persisten mientras el contenedor esté corriendo y nunca se guardan en el disco duro.

# Indicaciones
## Comandos

Empezamos instalando el api que se nos indico en clase "hello-world-api"
```bash
docker pull nmatsui/hello-world-api
```


Y clonamos las demas carpetas como el server.js, Dockerfile, config.js,etc.
```bash
git clone https://github.com/nmatsui/hello-world-api.git
```


Ejecutamos el contenedor 
```bash
docker run -d --rm -p 3000:3000 nmatsui/hello-world-api
```
Y en este caso se nos pidio 3 apis locales por lo que se uso los puertos 3000,3001 y 3002

Se utiliza docker compose para levantar y verificar que todo este corriendo
```bash
docker compose up -d
```
Se utiliza el --build como apoyo para limpiar cualquier residuo que quede en la cache
```bash
docker compose up --build
```

Se utilizo el comando curl para ir verificando que el mensaje se recibiera de forma correcta en este caso se utilizo "Hola Diego Rodriguez Becerra desde env"
```bash
curl.exe -i http://localhost:3000/
curl.exe -i http://localhost:3001/
curl.exe -i http://localhost:3002/
```

Adicionalmente se crearon los archivos .gitignore, .env, .env.example y docker-compose.yaml

## Configuración por entorno
```
MESSAGE= Hola Diego Rodriguez Becerra desde env
```
# Creditos
- Rodriguez Becerra Diego Arturo




