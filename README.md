# Gym App

## 1. VISIÓN GENERAL DEL PROYECTO
### 1.1 Propósito y Alcance
La plataforma web de gestión de gimnasios busca digitalizar y optimizar la operación de gimnasios mediante una solución centralizada para usuarios y administradores. Permitirá el registro de usuarios, reserva de clases, visualización de horarios, y administración de contenidos.

### 1.2 Stakeholders y Usuarios Objetivo
- Administradores del gimnasio
- Instructores o coordinadores de clases
- Usuarios del gimnasio

### 1.3 Beneficios Esperados
- Mejora de la experiencia del usuario
- Aumento en la tasa de asistencia y fidelización
- Gestión eficiente de cupos y recursos
- Reducción de trabajo administrativo manual

## 2. REQUISITOS DETALLADOS
### 2.1 Requisitos funcionales
| Módulo        | Requisitos    |
| ------------- | ------------- |
| Autenticación  | Registro, login, recuperación de contraseña, validación de email  |
| Dashboard  | Visualización de calendario, próximas clases, estadísticas  |
| Clases  | Listado filtrable por disciplina, horarios, capacidad, instructor |
| Reservas  | Alta/baja de reserva, historial, notificaciones |
| Perfil  | Ver/editar datos personales, cambiar contraseña  |
| Administración  | ABM de usuarios, disciplinas, clases y reservas  |

### 2.2 Requisitos No Funcionales

- **Rendimiento:** <200ms para respuesta de API crítica
- **Usabilidad:** Accesibilidad WCAG AA, diseño responsive

## 3. ARQUITECTURA DEL SISTEMA
### 3.1 Diagrama general
![image](https://github.com/user-attachments/assets/8155705b-f8f7-4c5c-a41e-bf9b3b057029)

### 3.2 Patrones de Diseño

- **MVC** (Modelo Vista Controlador)
- **Repository Pattern** (persistencia)
- **Singleton** para servicios comunes

### 3.3 Diagrama Entidad Relación
<img width="359" alt="image" src="https://github.com/user-attachments/assets/ed2dccad-b3d0-482a-97e5-dcc5a41a8a3b" />

## 4. ESPECIFICACIONES TÉCNICAS

### 4.1 Stack Tecnológico

- **Frontend:** React + Tailwind CSS
- **Backend:** Node.js + Express
- **Base de Datos:** PostgreSQL
- **Autenticación**: JWT

### 4.2 Frameworks y Librerías
| Propósito | Tecnología | Uso |
| :---         | :---      | :--- |
| UI   | React + Tailwind     | Modularidad + Velocidad de desarrollo    |
| API     | Express.js       | Simplicidad y compatibilidad      |
| Base de datos     | PostgreSQL       | Base de datos relacional por la estructura  |

## 5. DISEÑO DETALLADO POR MÓDULO

### 5.1 Módulo de Autenticación

- **Funcionalidad:** Registro, inicio de sesión, recuperación
- **Flujo:** Usuario completa formulario → API valida → crea usuario + token
- **Componentes:** Formulario, validación, notificaciones
- **Errores:** Email duplicado, email sin formato, contraseña inválida

### 5.2 Dashboard

- **Funcionalidad:** Visualizar calendario y estadísticas personales
- **Flujo:** Usuario logueado → API obtiene clases → se renderiza calendario
- **Datos:** clases próximas, total reservas, porcentaje de asistencia

### 5.3 Visualización de Clases

- **Funcionalidad:** Buscar, filtrar y explorar clases por disciplina
- **Componentes:** Filtros, tarjetas de clase, botón de reserva

### 5.4 Reservas

- **Funcionalidad:** Reservar o cancelar reserva
- **Flujo:** Usuario selecciona clase → API verifica cupo → crea reserva
- **Errores:** Sin cupo, horario conflictivo

### 5.5 Perfil

- **Funcionalidad:** Actualizar nombre, email, contraseña
- **Componentes:** Formulario editable, botón de guardar, feedback visual

# 6. DIAGRAMAS DE CASOS DE USO
![image](https://github.com/user-attachments/assets/7b6892c2-12c1-46db-aab7-639c864ed98e)
![image](https://github.com/user-attachments/assets/5853c52b-024d-4362-b733-219ba053bb78)
![image](https://github.com/user-attachments/assets/1e5d6a7b-7f3d-4bac-9c2c-0c9ee33fb85e)





