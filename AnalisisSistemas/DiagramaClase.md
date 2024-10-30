# ARCHIVOS PRIMERA ITERACIÓN

## CÓDIGO WSD

```js
@startuml

class Usuario {
    - nombreCompleto : String
    - apellidos : String
    - correoElectronico : String
    - contrasena : String
}

class Producto {
    - nombre : String
    - descripcion : String
    - costo : Float
    - cantidad : Int
}

class Inventario {
    - producto : Producto
    - proveedor : String
    - orden_compra : String
    - imagen : String
}

class Detalle_Factura {
    - descripcion : String
    - iva : Double
    - tipo_pago : String
    - factura : Factura
}

class Factura {
    - usuario : Usuario
    - producto : Producto
    - costo_envio : Float
    - total_compra : Float
}
@enduml

# EXPLICACION

Este diagrama uml representa la estructura de clases y sus relaciones para un sistema de gestión de facturas, inventario, y usuarios. Aquí está la explicación de cada componente:

##Clases principales:

 **Usuario**: Representa a los usuarios del sistema.
  
  - **Atributos**:
    - `nomCompleto`: Nombre completo del usuario.
    - `apellidos`: Apellidos del usuario.
    - `correoElectronico`: Correo del usuario.
    - `contrasena`: Contraseña del usuario.

Atributos: producto: Instancia de Producto. proveedor: Nombre del proveedor. orden_compra: Número de orden de compra. imagen: Imagen del producto. Detalle_Factura: Almacena información de cada ítem en la factura.

Atributos: descripcion: Descripción del detalle. IVA: Porcentaje de IVA aplicado. tipo_pago: Método de pago utilizado. factura: Instancia de Factura a la cual pertenece este detalle. Factura: Guarda la información general de la factura.

Atributos: usuario: Instancia de Usuario que hizo la compra. producto: Producto(s) comprados. costo_envio: Costo de envío. total_compra: Monto total de la compra. total_unitario: Precio unitario de cada producto. 


```