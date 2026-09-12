
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
- $ docker run --name some-postgres -e POSTGRES_PASSWORD=micontraseña -d
postgres

# Indicaciones
## Comandos


```bash
docker compose up -d
```

```bash
docker compose up --build
```
## Configuración por entorno
```
MESSAGE= Tarea de Laboratorio Semana 02/Rodriguez Becerra Diego Arturo/#000291000
```
# Creditos
- Rodriguez Becerra Diego Arturo




