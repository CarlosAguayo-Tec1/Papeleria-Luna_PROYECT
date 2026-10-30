# Papeleria-Luna_PROYECT
Inicio de proyecto grande para la gestión y sistema de control de un negocio de una papelería. Con cambio de modo (claro-oscuro))

# 🌙 Papelería Luna
### Sistema de gestión y administración de una papelería

## 📌 Descripción del proyecto

**Papelería Luna** es un sistema de escritorio desarrollado en Python, diseñado para facilitar la administración y el control de las operaciones de una papelería.

El sistema permite gestionar diferentes áreas del negocio, centralizando la información en una base de datos relacional y proporcionando una interfaz gráfica intuitiva para realizar las actividades administrativas y operativas.

El proyecto busca optimizar procesos como el registro de clientes, administración de empleados, control de inventario, gestión de proveedores, registro de ventas y administración de pedidos.

## 🎯 Objetivo general

Desarrollar un sistema informático que permita automatizar y mejorar la gestión administrativa y operativa de una papelería, mediante herramientas que faciliten el control de información, reduzcan errores en los procesos y agilicen las actividades diarias del establecimiento.

## ⚙️ Tecnologías utilizadas

| Tecnología | Descripción |
|---|---|
| Python | Lenguaje principal de programación. |
| Tkinter | Desarrollo de interfaces gráficas. |
| ttk | Componentes visuales y tablas. |
| MariaDB / MySQL | Gestión y almacenamiento de información. |
| mysql.connector | Conexión entre Python y la base de datos. |
| Visual Studio Code | Entorno de desarrollo. |

## 🚀 Funcionalidades principales

El sistema está compuesto por diferentes módulos que permiten administrar las operaciones de la papelería.

### 1. Gestión de clientes
- Registro de nuevos clientes.
- Consulta y visualización de clientes.
- Búsqueda por nombre e identificación.
- Modificación de información.
- Desactivación de registros.
- Recuperación de clientes desactivados.

### 2. Gestión de empleados
- Registro de empleados.
- Consulta de información.
- Búsqueda de empleados.
- Modificación de datos.
- Desactivación y recuperación de empleados.
- Visualización de información individual.

### 3. Gestión de proveedores
- Registro de proveedores.
- Consulta de información.
- Búsqueda por nombre e identificación.
- Modificación de datos.
- Desactivación de proveedores.
- Recuperación de registros.

### 4. Gestión de productos e inventario
- Registro y administración de productos.
- Clasificación por categorías.
- Asociación de productos con proveedores.
- Control de existencias.
- Configuración de niveles mínimos de stock.
- Identificación de productos con existencias bajas.
- Actualización de cantidades disponibles.
- Registro de movimientos de inventario.

### 5. Gestión de ventas
- Búsqueda y selección de productos.
- Administración de un carrito de compras.
- Asociación de ventas con clientes y empleados.
- Cálculo de importes.
- Selección de métodos de pago.
- Registro de ventas.
- Descuento automático de existencias.
- Consulta del historial de ventas.
- Visualización de detalles de cada venta.
- Cancelación de ventas.

### 6. Gestión de pedidos a proveedores
- Creación de pedidos.
- Asociación de pedidos con proveedores y empleados.
- Selección de productos y cantidades.
- Cálculo de subtotales y totales.
- Recepción parcial o completa de mercancía.
- Actualización automática del inventario al recibir productos.
- Cancelación de pedidos pendientes.
- Identificación de productos con existencias bajas.
- Consulta del historial de pedidos.

### 7. Gestión de usuarios y acceso
- Registro de cuentas de usuario.
- Validación de empleados.
- Autenticación mediante contraseña.
- Administración de rangos y permisos.
- Control del estado de las cuentas.

### 8. Configuración visual
- Interfaz gráfica personalizada.
- Modo claro y modo oscuro.
- Configuración de colores.
- Persistencia de preferencias visuales mediante la base de datos.

## 🗄️ Base de datos

El sistema utiliza una base de datos relacional denominada:

`Papeleria_Luna`

Entre las principales tablas que conforman la estructura de la base de datos se encuentran:

- `Clientes`
- `Empleados`
- `Proveedores`
- `Categorias`
- `Productos`
- `Ventas`
- `Detalle_Venta`
- `Pedidos_Proveedor`
- `Detalle_Pedido`
- `Movimientos_Inventario`
- `Alertas_Stock`
- `usuarios`
- `Configuracion`

La información se almacena y administra mediante MariaDB/MySQL, utilizando relaciones entre tablas para mantener la integridad de los datos.

## 🎨 Diseño de interfaz

La interfaz gráfica sigue una identidad visual propia de Papelería Luna, utilizando una combinación de colores que busca mantener una apariencia limpia, organizada y agradable.

**Paleta de colores principal:**

| Elemento | Color |
|---|---|
| Fondo | `#F1F5F9` |
| Paneles | `#FFFFFF` |
| Azul marino | `#172554` |
| Azul secundario | `#1E3A5F` |
| Naranja | `#F59E0B` |
| Verde azulado | `#0F766E` |
| Texto | `#1E293B` |
| Texto secundario | `#64748B` |
| Bordes | `#DBE3ED` |
| Rojo | `#EF4444` |

La aplicación utiliza la tipografía Arial y cuenta con una configuración de apariencia clara y oscura.

## 💻 Requisitos para ejecutar el proyecto

Antes de ejecutar el sistema es necesario contar con:

- Python 3 instalado.
- MariaDB o MySQL.
- Un entorno de desarrollo como Visual Studio Code.
- La biblioteca `mysql-connector-python`.

## 📥 Instalación y configuración

**1. Clonar el repositorio**

```bash
git clone URL_DEL_REPOSITORIO
```

**2. Acceder a la carpeta del proyecto**

```bash
cd Papeleria-Luna
```

**3. Instalar la dependencia necesaria**

```bash
pip install mysql-connector-python
```

**4. Configurar la base de datos**

Iniciar MariaDB/MySQL y crear la base de datos:

```sql
CREATE DATABASE Papeleria_Luna;
```

Posteriormente, importar la estructura SQL del proyecto para crear las tablas y relaciones correspondientes.

**5. Configurar la conexión**

Verificar que los parámetros de conexión utilizados por los módulos coincidan con la configuración de MariaDB/MySQL:

```python
DB_CONFIG = {
    "host": "localhost",
    "user": "root",
    "password": "",
    "database": "Papeleria_Luna",
    "connection_timeout": 10
}
```

Es importante ajustar las credenciales de acuerdo con la configuración del entorno donde se ejecutará el sistema.

**6. Ejecutar la aplicación**

Abrir el archivo principal del proyecto desde Python o Visual Studio Code.

## 🔐 Seguridad y administración

El sistema contempla mecanismos de control de acceso mediante usuarios, rangos y estados de cuenta.

Las contraseñas se manejan mediante un proceso de derivación basado en PBKDF2, evitando almacenarlas directamente como texto sin protección.

También se utilizan mecanismos de desactivación lógica para conservar determinados registros históricos sin eliminarlos permanentemente.

## 📊 Alcance del proyecto

Papelería Luna integra diferentes procesos administrativos y operativos dentro de una misma aplicación, permitiendo mantener un mejor control de:

- Información de clientes y empleados.
- Registro y administración de proveedores.
- Productos y existencias.
- Operaciones de venta.
- Pedidos y recepción de mercancía.
- Movimientos de inventario.
- Usuarios y configuración del sistema.

## 👨‍💻 Desarrollo

Este proyecto fue desarrollado con fines académicos y como una aplicación práctica de programación, desarrollo de interfaces gráficas, programación orientada a objetos, conexión con bases de datos y administración de información.

## 📄 Licencia

Este proyecto es de carácter académico. Los derechos de uso, distribución y modificación deberán establecerse mediante la licencia que se incorpore al repositorio.

---

**Papelería Luna**  
*Organización, control y administración en un solo lugar.* 🌙
