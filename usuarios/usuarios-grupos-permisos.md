# Gestion de Usuarios y Grupos

En este documento vamos a recopilar al detalle los usuarios que existen en nuestra empresa a si como los grupos. Tambien haremos un segimiento de los permisos y controles implementados. 


## Usuarios

En este apartado podemos ver los usuarios que contienen nuestra empresa de forma detallada indicando los permisos que tienen los usuarios.
El principio por el cual hemos decidido como asignar los permisos es el de minimo privilegio dandole a cada miembro de la plantilla el minimo acceso indispensable para el desempeño de su puesto de trabajo.

### 1. Usuario Comercial
- **Nombre:** Alejandro Torres
- **Correo:** comercial@littletous.es
- **Tipo de usuario:** Usuario interno
- **Permisos:**
    - Ventas: Solo mostrar su documentos propios
    - Facturación: Ninguno
    - Inventario: Usuario
- **Justificación:** Responsable de la prospección comercial y la elaboración de presupuestos iniciales. Por eso no requiere accesos a los datod cntables ni a los presupuestos del resto de la plantilla.


### 2. Usuario Ventas
- **Nombre:** Sofía Ramírez
- **Correo:** ventas@littletous.es
- **Tipo de usuario:** Usuario interno
- **Permisos:**
    - Ventas: Administrador
    - Facturación: Mostrar importes / Solo lectura
    - Inventario: Usuario
- **Justificación:** Coordina los presupuestos del equipo comercial, autoriza ofertas y puede consultar el estado de las facturas de los clientes sin poder modificarla. 


### 3. Usuario Facturación
- **Nombre:** Paula Rivas
- **Correo:** facturacion@littletous.es
- **Tipo de usuario:** Usuario interno
- **Permisos:**
    - Ventas: Mostrar todos los documentos
    - Facturación: Responsable
    - Inventario: Ninguno
- **Justificación:** Al ser encargada del fuljo financiero no tiene que tiene que tener que realizar ninguna función de ventas o inventario, pero es necesario que pueda realizar todas las funciones de facturación como: generar facturas de pedidos confirmados, validación, contabilización y resgistro de cobros.

### 4. Usuario (Portal)
- **Nombre:** Laura Gómez Martínez
- **Correo:** laura.gomez@gmail.es
- **Tipo de usuario:** Usuario portal
- **Permisos:** Sin acceso a la parte administrativa. 
- **Justificación:** Permite al cliente acceder de la web para consultar sus pedidos pero sin entrar a la partes administrativa de la empresa.

### Tabla Resumen 

Nos encontramos con un resumen mas visual de los Usuarios y sus pribilegios:

| Usuario | Nombre | Correo | Rol | Tipo | Permiso Ventas | Permiso Facturación | Permiso Inventario |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Alejandro Torres | comercial@littletous.es | Comercial | Interno | Mostrar solo sus documentos | Ninguno | Usuario |
| 2 | Sofía Ramírez | ventas@littletous.es | Ventas | Interno | Administrador | Mostrar importes | Usuario |
| 3 | Paula Rivas | facturacion@littletous.es | Facturación | Interno | Ninguno | Responsable | Mostrar documentos |
| 4 | Laura Gómez Martínez | laura.gomez@gmail.es | Cliente | Portal | Acceso portal propio  | Acceso portal propio | Ninguno |


---
## Grupos

En esta parte podemos ver las configuraciones que vamos a realizar al grupo comercial sin la necesidad de otrogar permisos globales:

### Ficha de Grupo

- **Nombre:** 'Little Tous / Comercial Junior'
- **Herencia:** Ventas / Mostrar solo sus documentos
- **Usuarios:** Alejandro Torres (comercial@littletous.es)

### Permisos

Se han definido reglas específicas para que el usuario pueda trabajar de forma autónoma con los contactos y los presupuestos, pero restringiendo la eleminación y edicion de configuraciones críticas

| Permiso | Estado | Justificación de Negocio | 
| :--- | :--- | :--- |
| Lectura | Marcado | Permire consultar sus presupuestos y pedidos |
| Escritura | Marcado | Permite modificar los presuspuestos y pedidos |
| Creación | Marcado | Premite la creacion de nuevos presupuestos de los clientes |
| Eliminación | Desmarcado | Se prohíbe el borrado de presupuestos para evitar la perdida de registros |


