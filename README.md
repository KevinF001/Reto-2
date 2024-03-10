# Reto-2
# Tienda online de Tecnologia
```mermaid
classDiagram
    class Tienda{
        + Nombre: string
        + ID: string
        + Productos: Producto
        + Formas de envío: Envio
    }
    class Cliente{
        + Nombre: string
        + Edad: int
        + Nacionalidad: string
        + Lugar de residencia: string
        + Dinero: float
        - Metodo de pago()
        - Opciones de descuento()
    }
    class Producto{
        + Tipo: string
        + Nombre: string
        + Precio: float
        - Disponibilidad()
    }
    class Celulares{
        + Marca: string
        + Modelo: string
        + Precio: float
    }
    class Portatiles{
        + Marca: string
        + Modelo: string
        + Precio: float
    }
    class Televisores{
        + Marca: string
        + Modelo: string
        + Precio: float
    }
    class Computadores{
        + Marca: string
        + Modelo: string
        + Precio: float
    }
    class Envios{
        + Paises disponibles: string
        + Producto: string
        + Transportadores: string
        - Costos()
        - Descuentos()
        - Fecha estimada de entrega()
    }
    class Envio{
        + Dirección: string
        + Empresa transportista: string
        - Disponibilidad_pais()
        - Disponibilidad_ciudad()
    }
    class Compra{
        + Productos: string
        + Costos: float
        + Costos de envío: float
        - Metodo de pago()
    }
    Tienda --* Producto
    Tienda"1" --> "1" Cliente
    Cliente -->  Compra : busca
    Celulares --|> Producto
    Portatiles --|> Producto
    Computadores --|> Producto
    Televisores --|> Producto
    Compra --* Producto
    Compra --* Envio
    Tienda --* Envios
    Envio --|> Envios
```
