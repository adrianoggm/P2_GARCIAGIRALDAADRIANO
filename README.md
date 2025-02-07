# Práctica 2: Orquestación de Servicios Web utilizando WS-BPEL

Este repositorio contiene el desarrollo de la **Práctica 2** de orquestación de servicios web utilizando *WS-BPEL* con **Oracle JDeveloper** y **SOA Suite**.

## Descripción

La práctica se centra en la implementación de dos procesos de negocio utilizando *WS-BPEL*:

### Reserva de Vuelos
Un proceso BPEL que gestiona la reserva de billetes de avión en función del tipo de empleado y los precios de diferentes aerolíneas.

### Regateo de Precios
Un sistema de negociación de precios entre un comprador y un vendedor, que incluye validación de disponibilidad de productos y generación de contraofertas.

## Requisitos Previos

- **Oracle JDeveloper 12c** instalado y configurado.
- **Oracle SOA Suite** correctamente configurado.
- **WebLogic Server** configurado para el despliegue.
- Conocimientos básicos de **BPEL**, **WSDL** y **SOAP**.

## Estructura del Proyecto

El proyecto está estructurado de la siguiente manera:

```bash
.
├── FlightServicesProject/      # Proyecto SOA para la Reserva de Vuelos
│   ├── FlightComposite/        # Compuesto SOA
│   │   ├── Empleado.bpel       # Determina el tipo de billete según el empleado
│   │   ├── Iberia.bpel         # Consulta y calcula el precio de vuelos con Iberia
│   │   ├── Vueling.bpel        # Consulta y calcula el precio de vuelos con Vueling
│   │   ├── Gestor.bpel         # Orquesta las interacciones entre los servicios
│   │   ├── *.wsdl              # Definición de servicios WSDL
│   │   ├── Composite.xml       # Configuración del compuesto SOA
│   └── test/                   # Casos de prueba SOAP
├── ShoppingServiceProject/      # Proyecto SOA para el Regateo de Precios
│   ├── ShoppingComposite/       # Compuesto SOA
│   │   ├── VerCantidad.bpel     # Verifica disponibilidad de productos
│   │   ├── Comprador.bpel       # Evalúa ofertas del comprador
│   │   ├── Vendedor.bpel        # Genera contraofertas del vendedor
│   │   ├── Gestor.bpel          # Coordina el proceso de regateo
│   │   ├── *.wsdl               # Definición de servicios WSDL
│   │   ├── Composite.xml        # Configuración del compuesto SOA
│   └── test/                    # Casos de prueba SOAP
└── README.md                    # Este archivo
```
## Instalación y Configuración

```bash
# Abrir Oracle JDeveloper 12c
# Importar los proyectos SOA (FlightServicesProject y ShoppingServiceProject)
# Asegurarse de que Oracle SOA Suite está en ejecución
# Configurar y desplegar los proyectos en WebLogic Server
# Utilizar SOAP-UI o el analizador HTTP de JDeveloper para probar los servicios
```
$ Se han definido varios casos de prueba para validar el funcionamiento de los procesos:

Reserva de Vuelos:
  - Empleados de diferente categoría (turista, business, jet privado).
  - Comparación de precios entre Iberia y Vueling.
  - Validación de fechas de vuelo.

Regateo de Precios:
  - Verificación de stock antes de negociar.
  - Diferentes ofertas y contraofertas entre comprador y vendedor.
  - Pruebas de aceptación y rechazo de precios.


