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
    
    
## Ubicación del docker-compose

- El archivo docker-compose indicado en el planteamiento se encuentra en la siguiente ruta: [docker-compose](https://github.com/testJgSf/project-setup/blob/develop/docker-compose.yml)     
## Contratos  de los servicios

### OpenAPI 3.0 (Swagger)  
  - calculator  [Servicio de cálculos](https://app.swaggerhub.com/apis-docs/test_jg_sf/calculator-service/1.0.0)  
 - sum  [Servicio de suma](https://app.swaggerhub.com/apis-docs/test_jg_sf/sum-service/1.0.0)  
- subtraction  [Servicio de resta](https://app.swaggerhub.com/apis-docs/test_jg_sf/subtraction-service/1.0.0)  
- multiplication  [Servicio de multiplicación](https://app.swaggerhub.com/apis-docs/test_jg_sf/multiplication-service/1.0.0  )  
- division  [Servicio de division](https://app.swaggerhub.com/apis-docs/test_jg_sf/division-service/1.0.0  ) 


### Colecciones Postman
- Dentro de cada colección de postman existen dos carpetas, local y cloud que referencia a la ejecución en GCP de la 
aplicación, es importante acotar que se ejecuta en la cuota gratuita.

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
  
## CI / CD
Cada microservicio tiene configurado un pipeline que cubre los pasos básicos cd CI/CD, la tecnología usada es Github 
actions, el deploy es hecho a servicios de GCP. A continuación el estado de cada microservicio:

- [Servicio de suma](https://github.com/testJgSf/sum-service/actions?query=workflow%3A%22Build+and+deploy+Dev+Env%22)   ![Build and deploy Dev Env](https://github.com/testJgSf/sum-service/workflows/Build%20and%20deploy%20Dev%20Env/badge.svg?branch=develop)
- [Servicio de resta](https://github.com/testJgSf/subtraction-service/actions?query=workflow%3A%22Build+and+deploy+Dev+Env%22) ![Build and deploy Dev Env](https://github.com/testJgSf/subtraction-service/workflows/Build%20and%20deploy%20Dev%20Env/badge.svg?branch=develop) 
- [Servicio de multiplicación](https://github.com/testJgSf/multiplication-service/actions?query=workflow%3A%22Build+and+deploy+Dev+Env%22)  ![Build and deploy Dev Env](https://github.com/testJgSf/multiplication-service/workflows/Build%20and%20deploy%20Dev%20Env/badge.svg?branch=develop)
- [Servicio de division](https://github.com/testJgSf/division-service/actions?query=workflow%3A%22Build+and+deploy%22)  ![Build and deploy](https://github.com/testJgSf/division-service/workflows/Build%20and%20deploy/badge.svg?branch=develop) 
- [calculator-service](https://github.com/testJgSf/calculator-service/actions?query=workflow%3A%22Build+and+deploy+Dev+Env%22)  ![Build and deploy Dev Env](https://github.com/testJgSf/calculator-service/workflows/Build%20and%20deploy%20Dev%20Env/badge.svg?branch=develop)
     

### Pruebas de integración
[Pruebas Integracion Postman](https://github.com/testJgSf/calculator-documentation/tree/develop/integrations-tests)  
   
### Más información  
Cualquier información extra contacte a José Gabriel Ortiz.