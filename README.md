# Repositorio para Arquitectura Web
## Segundo cuatrimetre 2024
## Juan Falcone
### Recursos accesibles (y posibles filtros)
- Estacion
  - por Barrio
    - /barrio/:barrio_id/estacion/
  - por cupos vacíos
    - /estacion/?cupos=X
  - por bicis en necesidad de reparación
    - /bicicletas/paraReparar/estacion/
  - por historial de bici
    - /bicicletas/:bici_id/estacions/
- Retiro
  - por abierto o cerrado
    - /retiro/?open=(TRUE|FALSE)
  - por usuario
    - /usuario/:user_id/retiros/
  - por estacion de salida
    - /estacion/:estacion_id/retiros/
- Bicicleta
  - por estacion
    - /estacion/:estacion_id/bicicletas/
  - por usuario que la haya utilizado
    - /usuario/:usuario_id/bicicletas/
  - por necesidad de reparación
    - /bicicletas/paraReparar/
- Usuario
  - por bicicleta utilizada
    - /bicicleta/:bicicleta_id/usuarios/
  - por deuda
    - /usuario/?deuda=X
  - por historial de deudas
    - /usuario/?deudaAcumulada=X
  - por utilizacion de estacion
    - /estacion/:estacion_id/usuarios/
### Métodos Post
- Retirar Bicicleta
  - Dado usuario y bicicleta, crea un ticket
### Métodos Patch
- Depositar bicicleta
  - Dado una estación y un estado de la bicicleta, actualiza el ticket y en caso de ser necesario penaiza al usuario
