# Repositorio para Arquitectura Web
## Segundo cuatrimetre 2024
## Juan Falcone
### Recursos accesibles (y posibles filtros)
- Estacion
  - por Barrio
    - GET /barrio/:barrio_id/estacion/
  - por cupos vacíos
    - GET /estacion/?cupos=X
  - por bicis en necesidad de reparación
    - GET /bicicletas/paraReparar/estacion/
  - por historial de bici
    - GET /bicicletas/:bici_id/estacions/
- Retiro
  - por abierto o cerrado
    - GET /retiro/?open=(TRUE|FALSE)
  - por usuario
    - GET /usuario/:user_id/retiros/
  - por estacion de salida
    - GET /estacion/:estacion_id/retiros/
- Bicicleta
  - por estacion
    - GET /estacion/:estacion_id/bicicletas/
  - por usuario que la haya utilizado
    - GET /usuario/:usuario_id/bicicletas/
  - por necesidad de reparación
    - GET /bicicletas/paraReparar/
- Usuario
  - por bicicleta utilizada
    - GET /bicicleta/:bicicleta_id/usuarios/
  - por deuda
    - GET /usuario/?deuda=X
  - por historial de deudas
    - GET /usuario/?deudaAcumulada=X
  - por utilizacion de estacion
    - GET /estacion/:estacion_id/usuarios/
### Métodos Post
- Retirar Bicicleta
  - Dado usuario y bicicleta, crea un ticket
    - POST /retiro/ {user_id,bicicleta_id}
### Métodos Patch
- Depositar bicicleta
  - Dado una estación, una bicicleta y un estado de la bicicleta, actualiza el ticket y en caso de ser necesario penaiza al usuario
    - PATCH /retiro/ {estacion_id, bicicleta_id, estado_bicicleta}
