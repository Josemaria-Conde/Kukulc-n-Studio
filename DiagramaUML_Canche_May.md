# Diagrama de clases UML por Juan Angel Canché Gongora y Christopher May Paat

---
El siguiente diagrama de clases presenta el funcionamiento del sistema.

![Diagrama UML](/Diagrama-christopher/Diagrama-UML/Diagrama-UML.jpeg)

---
## Explicación del diagrama

**Entidades y Requisitos del Proyecto**

---
### 1. Usuario
**Entidad:** Usuario  

**Requisitos Relacionados:**
- **RF-001:** Inicio de sesión con usuario y contraseña.
- **RF-019:** Registro de nuevos usuarios.
- **RNF-007:** Protección de credenciales mediante encriptación.
- **RNF-016:** Posibilidad de activar o desactivar la música y efectos de sonido.

**Justificación:**
- **Relación con Perfil:** Un Usuario puede tener múltiples Perfiles para gestionar diferentes partidas guardadas. (1 usuario puede tener muchos perfiles, y un perfil pertenece a un solo usuario).
- **Operaciones:** Métodos como `crearCuenta()`, `iniciarSesion()`, `cerrarSesion()` y `verificarLogin()` cumplen con RF-001 y RF-019, garantizando la seguridad mediante la encriptación de contraseñas (RNF-007).
