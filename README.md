# Sistema de Gestión de Ventas y Reportes

Sistema web para la gestión de Ventas de los productos que ofrece la empresa y para la gestión de Reportes de productos más vendidos,
cuál es el método de pago más usado, cuantos fueron las ganancias (al día, semana y mes), entre otros.

Desarrollo como proyecto final del curso de Java Web en SENATI

## Descripción del negocio

__Empresa:__ Recepciones y Eventos Gale E.I.R.L.

__Nombre comercial:__ El Rincón de Rango

__RUC:__ 20614373203

__Giro del negocio:__ Restobar - Establecimiento dedicado a la venta decomidas y bebidas, con atención en mesa mediante mozos
y eventos con música en vivo los fines de semana.

__Tamaño:__ Microempresa con más de 10 trabajadores (mozos, cajero, cocineros, administrador y contador externo).

__Contexto actual:__ El negocio opera de forma mayormente manual: los pedidos se anotan en papel o se comunican de voz a la cocina, 
el inventario se controla en un cuaderno, y calcular las ganancias diarias resulta complicado y toma bastante tiempo. 
Acepta múltiples métodos de pago (efectivo, tarjeta, Yape, Plin, transferencia), pero no cuenta con un sistema digital que
centralice las ventas ni genere reportes automáticos.

__Justificación del proyecto:__ El dueño reportó todos los problemas listados en la entrevista emitida para la obtención de datos: 
pedidos olvidados, platos equivocados, falta de control de insumos, dificultad para conocer las ventas del día, pérdida de dinero e insumos, 
demoras por mala comunicación y errores en cobros.
Esto evidencia una necesidad urgente de digitalizar al menos el proceso de ventas y generación de reportes para 
reducir pérdidas, errores y tiempos muertos.

## Indetificar el problema y solución

### Problema delimitado:

El Rincón de Rango no cuenta con ningún sistema digital para registrar sus ventas. Todo el proceso, desde la 
toma del pedido hasta el cobro, se realiza de forma manual (papel, voz, memoria), lo que genera:

- Errores frecuentes en pedidos (platos equivocados, pedidos olvidados).
- Imposibilidad de conocer las ventas reales al final del día, semana o mes (el dueño indica que "es complicado y toma bastante tiempo").
- Pérdida de dinero e insumos sin poder rastrear el origen.
- Errores en cobros y dificultad para cuadrar caja.

En resumen: __No existe trazabilidad ni control sobre el flujo de ventas,__ lo que impide tomar 
decisiones informadas y genera pérdidas económicas constantes.

### Solución tecnológica propuesta:

Desarrollar un __Sistema Web de Gestión de Ventas y Reportes__ que permita:

1. Registrar digitalmente cada venta (productos, cantidades, precios, método de pago, mozo responsable).
2. Generar reportes automáticos de ventas por día, semana y mes.
3. Gestionar el catálogo de productos (platos y bebidas) con precios y disponibilidad.
4. Controlar la caja diaria con resumen de ingresos por método de pago.

__Justificación tecnológica:__ Al ser un sistema web, es accesible desde cualquier dispositivo que ya posee 
el negocio (laptop, tablets, celulares) sin necesidad de instalar software adicional. El internet del local 
es estable ("muy bueno, casi nunca se cae"), lo que garantiza la viabilidad de una solución basada en la nube/web o también solo local.

## Requerimientos Funcionales (RF)

| Código | Descripción |
|---|---|
| __RF-01__ | El sistema debe registrar una nueva venta asociando los productos consumidos, las cantidades, el precio unitario, el mozo responsable y el método de pago utilizado. |
| __RF-02__ | El sistema debe generar reportes de ventas filtrados por día, semana y mes, mostrando totales de ingresos, cantidad de ventas y desglose por método de pago. |
| __RF-03__ | El sistema debe gestionar el catálogo de productos (crear, editar, eliminar y listar platos y bebidas) con su nombre, precio, categoría y estado de disponibilidad. |
| __RF-04__ | El sistema debe controlar la apertura y cierre de caja diaria, calculando automáticamente el total de ingresos y el desglose por cada método de pago (efectivo, tarjeta, Yape, Plin, transferencia). |
| __RF-05__ | El sistema debe autenticar a los usuarios mediante credenciales (usuario y contraseña) y restringir el acceso según su rol (administrador, cajero, mozo), permitiendo que solo el administrador acceda a los reportes de ventas y configuración del sistema. |

## Requerimientos No Funcionales (RNF)

| Código | Tipo | Descripción |
|---|---|---|
| __RNF-01__ | __Usabilidad__ | La interfaz del sistema debe ser intuitiva y sencilla, permitiendo que un mozo sin experiencia técnica pueda registrar una venta en menos de 1 minuto y sin capacitación extensa. |
| __RNF-02__ | __Rendimiento__ | El sistema debe cargar cualquier página y procesar el registro de una venta en un tiempo máximo de 3 segundos, incluso en horas punta con múltiples usuarios concurrentes (más de 10 trabajadores). |
| __RNF-03__ | __Seguridad__ | El sistema debe encriptar las contraseñas de los usuarios, manejar sesiones con tokens seguros y garantizar que la información de ventas, ganancias y datos del negocio solo sea accesible según los permisos del rol asignado. |
| __RNF-04__ | __Compatibilidad__ | El sistema debe ser responsive y funcionar correctamente en los navegadores web de los dispositivos disponibles en el local (laptop, tablet y celulares), sin requerir instalación de software adicional. |

## Diagrama Entidad-Relación (DER)

<img width="1274" height="741" alt="DER restobar" src="https://github.com/user-attachments/assets/6b19d3bd-1935-49a9-8efe-33221e7078f2" />

## Modelo Relacional (MR)

<img width="1133" height="751" alt="MR restobar" src="https://github.com/user-attachments/assets/f3e33b91-9efb-4f2e-a021-dd39a13221a9" />



