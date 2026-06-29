# 🐾 Pet Manager - Tienda de Mascotas

Proyecto académico desarrollado para **Programación III** de la **Tecnicatura Universitaria en Programación - UTN**.

La aplicación consiste en un sistema web simple para gestionar mascotas. Permite registrar nuevas mascotas, listar los registros existentes, buscar por nombre o especie y navegar los resultados mediante paginación.

---

## 🎯 Objetivo del proyecto

El objetivo principal fue aplicar conceptos de Laravel en un CRUD funcional, utilizando:

* Rutas web
* Controladores
* Modelos Eloquent
* Migraciones
* Seeders y Factories
* Validaciones
* Vistas Blade
* Paginación

---

## 🧰 Tecnologías utilizadas

| Herramienta       | Uso                  |
| ----------------- | -------------------- |
| Laravel 13        | Framework backend    |
| PHP 8.3+          | Lenguaje principal   |
| MYSQL          | Base de datos local  |
| Blade             | Motor de plantillas  |
| CSS personalizado | Diseño visual        |
| Vite              | Compilación frontend |
| Faker             | Datos de prueba      |

---

## ✨ Funcionalidades principales

* Registrar mascotas con nombre, especie y edad.
* Validar los datos antes de guardar.
* Listar mascotas en una tabla.
* Buscar mascotas por nombre o especie.
* Paginar resultados para mejorar la visualización.
* Mostrar mensajes de confirmación al registrar datos.
* Generar mascotas de prueba con seeders.

---

## 🗄️ Estructura de la base de datos

### Tabla `pets`

| Campo        | Tipo            | Función                |
| ------------ | --------------- | ---------------------- |
| `id`         | BIGINT UNSIGNED | Identificador único    |
| `name`       | VARCHAR         | Nombre de la mascota   |
| `species`    | VARCHAR         | Especie de la mascota  |
| `age`        | INTEGER         | Edad                   |
| `created_at` | TIMESTAMP       | Fecha de creación      |
| `updated_at` | TIMESTAMP       | Fecha de actualización |

La tabla se crea mediante una migración de Laravel. Esto permite versionar la estructura de la base de datos y replicarla fácilmente en otro entorno.

---

## 🌱 Datos de prueba

El proyecto utiliza una Factory para generar mascotas falsas con Faker.

Comando:

```bash
php artisan db:seed
```

Esto crea 50 mascotas de prueba para probar el listado, la búsqueda y la paginación.

---

## 🚀 Instalación del proyecto

```bash
git clone https://github.com/apolobenitez65-prog/Tienda-de-Mascotas
cd Tienda-de-Mascotas
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
php artisan serve
```

Luego abrir en el navegador:

```bash
http://127.0.0.1:8000
```

En PowerShell, si `npm install` da error por políticas de scripts, usar:

```bash
npm.cmd install
npm.cmd run dev
```

---

## 📁 Estructura principal

```text
app/
├── Http/Controllers/
│   └── PetController.php
├── Models/
│   └── Pet.php

database/
├── factories/
│   └── PetFactory.php
├── migrations/
│   └── create_pets_table.php
└── seeders/
    └── DatabaseSeeder.php

resources/views/
├── layouts/
│   └── app.blade.php
├── pets/
│   ├── index.blade.php
│   └── create.blade.php
└── components/

routes/
└── web.php
```

---

## 🧪 Rutas del sistema

| Método | Ruta              | Acción                   |
| ------ | ----------------- | ------------------------ |
| GET    | `/`               | Lista las mascotas       |
| GET    | `/mascotas`       | Lista las mascotas       |
| GET    | `/mascotas/crear` | Formulario de registro   |
| POST   | `/mascotas`       | Guarda una nueva mascota |

---

## 🧠 Conceptos aplicados

Durante el desarrollo se trabajó con:

* **Migraciones:** creación de la tabla `pets`.
* **Modelo Eloquent:** representación de la tabla en Laravel.
* **Factory:** generación automática de datos falsos.
* **Seeder:** carga inicial de datos de prueba.
* **Validaciones:** control de datos antes de guardar.
* **Blade:** separación entre lógica y vista.
* **Paginación:** mejora en la navegación del listado.

---

## 👨‍💻 Autor

**BENITEZ APOLO**
Tecnicatura Universitaria en Programación - UTN
