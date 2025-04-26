# CodeIgniter 4.6 Docker Setup

Este es un entorno Docker para CodeIgniter 4.6 que incluye:
- PHP 8.1 con Apache
- MySQL 8.0
- Todas las extensiones PHP necesarias para CodeIgniter 4

## Requisitos
- Docker
- Docker Compose

## Instalación

1. Clonar el repositorio:
```bash
git clone <tu-repositorio>
cd <tu-repositorio>
```

2. Copiar el archivo de entorno:
```bash
cp env .env
```

3. Iniciar los contenedores:
```bash
docker-compose up -d
```

4. Instalar dependencias de CodeIgniter:
```bash
docker-compose exec app composer install
```

## Acceso
- Aplicación: http://localhost:8080
- Base de datos:
  - Host: db
  - Puerto: 3306
  - Usuario: ci4_user
  - Contraseña: db_password
  - Base de datos: ci4_db

## Comandos útiles
```bash
# Ver logs
docker-compose logs -f

# Detener contenedores
docker-compose down

# Reconstruir contenedores
docker-compose up -d --build
```
