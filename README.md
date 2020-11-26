# Calculadora sobre microservicios

## Planteamiento inicial
[Ejercicio](https://github.com/JosephCastro/Katas/blob/master/Calculadora.md)
  
## ¿Cómo ejecutar?
### Configuración en 1 min. (Requisito tener instalado Docker) (1 min con buen internet :stuck_out_tongue_winking_eye:)
1) Clonar el proyecto de setup desde el siguiente enlace: [Setup](https://github.com/testJgSf/project-setup) con:
 
>      git clone https://github.com/testJgSf/project-setup

2) Entrar a la carpeta project-setup con el comando `cd project-setup`  
3) Ejecutar el script setUp.sh  con el comando `./setUp.sh`  
4) Esperar que se termine de ejecutar el script, comprobar su ejecución correcta ejecutando `docker ps` y debería tener como salida los 5 servicios corriendo.  
  
### Sin Docker  
- Se require tener instalado nodeJs v12.13.0  
- Ingresar a los [componentes](#componentes) y seguir las instrucciones de su readme de forma individual.
    
## Contratos  de los servicios

### OpenAPI 3.0 (Swagger)  
  - calculator  [Servicio de cálculos](https://app.swaggerhub.com/apis-docs/test_jg_sf/calculator-service/1.0.0)  
 - sum  [Servicio de suma](https://app.swaggerhub.com/apis-docs/test_jg_sf/sum-service/1.0.0)  
- subtraction  [Servicio de resta](https://app.swaggerhub.com/apis-docs/test_jg_sf/subtraction-service/1.0.0)  
- multiplication  [Servicio de multiplicación](https://app.swaggerhub.com/apis-docs/test_jg_sf/multiplication-service/1.0.0  )  
- division  [Servicio de division](https://app.swaggerhub.com/apis-docs/test_jg_sf/division-service/1.0.0  ) 


### Colecciones Postman
[Colecciones de postman](https://github.com/testJgSf/calculator-documentation/tree/develop/postman-collections)  
  
## Componentes  
El proyecto está compuesto por 5 microservicios, 4 de operaciones básicas (=,-*,/) y un servicio de orquestación.
  
- sum  [Servicio de suma](https://github.com/testJgSf/sum-service)  
- subtraction  [Servicio de resta](https://github.com/testJgSf/subtraction-service)  
- multiplication  [Servicio de multiplicación](https://github.com/testJgSf/multiplication-service)  
- division  [Servicio de division](https://github.com/testJgSf/division-service)  
- Servicio de Orquestación [calculator-service](https://github.com/testJgSf/calculator-service) 
    
## Diagrama de la solución  
  
![Solution](https://github.com/testJgSf/calculator-documentation/blob/develop/diagrams/calculatorSolutionDesign.png?raw=true)
  
### Pruebas de integración
[Pruebas Integracion Postman](https://github.com/testJgSf/calculator-documentation/tree/develop/integrations-tests)  
  
   
### Más información  
Cualquier información extra contacte a José Gabriel Ortiz.