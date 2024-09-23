# Repositorio para Arquitectura Web
## Segundo cuatrimetre 2024
## Juan Falcone
### Recursos accesibles (y posibles filtros)
- Estacion
  - por Barrio
  - por cupos vacíos
  - por bicis en necesidad de reparación
  - por historial de bici
- Retiro
  - por abierto o cerrado
  - por usuario
  - por estacion de salida
- Bicicleta
  - por estacion
  - por usuario que la haya utilizado
  - por necesidad de reparación
- Usuario
  - por bicicleta utilizada
  - por deuda
  - por historial de deudas
  - por utilizacion de estacion
### Métodos Post
- Retirar Bicicleta
  - Dado usuario y bicicleta, crea un ticket
### Métodos Patch
- Depositar bicicleta
  - Dado una estación y un estado de la bicicleta, actualiza el ticket y en caso de ser necesario penaiza al usuario
