# Documento de Pruebas

## 1. Descripcion del Sistema
Es una aplicación que permite a los estudiantes registrarse y participar en eventos organizados por la universidad. El sistema valida la información ingresada, incluyendo el código estudiantil, antes de permitir la inscripción. Facilita la gestión y control de participantes en cada evento. Garantiza que solo estudiantes con códigos válidos puedan acceder a las actividades.

## 2. Requerimientos a Evaluar
RF - 2 Codigo estudiante

## 3. Tecnicas de Prueba Aplicadas
Requerimiento Funcional 1: 
Escogí dos tecnicas combinadas:

- **Particion de Equivalencia (PE)**
- **Analisis de Valores Limite (AVL)**
Porque el requerimiento trata de un rango numerico, y estas dos tecnicas son las que mejor se ajustan a ese tipo de condicion.

Con la **Particion de Equivalencia** se agrupan los valores que el sistema trata igual, lo que permite reducir la cantidad de pruebas sin perder cobertura. En este caso hay tres grupos: valores por debajo del rango, dentro del rango y por encima.

Con el **Analisis de Valores Limite** se prueban los bordes exactos del rango, porque ahi es donde suelen aparecer los errores (por ejemplo, usar < en vez de <=). Probar 15, 16, 65 y 66 cubre esos puntos criticos.

Requerimiento Funcional 2:
Particion de equivalencias
La particion de equivalencias es la mejor opción ya que el RF-02 define restricciones con fronteras claras como la longitud, carácter inicial y tipo de caracteres, lo que permite agrupar las entradas en clases donde todos los valores se comportan igual, haciendo innecesario probar cada dato individualmente. Así, en lugar de probar cientos de combinaciones, basta con representar cada clase con un solo caso, logrando máxima cobertura con el mínimo de pruebas posible.
RF-01 Registro de Estudiante (Edad)

## 4. Casos de Prueba Diseñados
| Criterio                | Clases válidas (V)                                   | Clases inválidas (I)                                                  |
|--------------------------|------------------------------------------------------|------------------------------------------------------------------------|
| Longitud del código      | V1: Exactamente 8 caracteres                         | I1: Menos de 8 caracteres                                             |
|                          |                                                      | I2: Más de 8 caracteres                                               |
| Carácter inicial         | V2: Inicia con la letra "E" mayúscula               | I3: Inicia con una letra distinta a "E"                               |
|                          |                                                      | I4: Inicia con "e" minúscula                                          |
|                          |                                                      | I5: Inicia con un carácter no alfabético                              |
| Caracteres restantes     | V3: Los 7 caracteres siguientes son numéricos       | I6: Contiene al menos una letra en los 7 caracteres                   |
|                          |                                                      | I7: Contiene al menos un carácter especial en los 7 caracteres        |
|                          |                                                      | I8: Contiene espacios en los 7 caracteres                             |

## 5. Trazabilidad
| Requerimiento  | Tecnica aplicada  |Justificacion|Casos Asociados|
| ------------- |:-------------:|:-------------:|:-------------:|
| RF1  | Analisis de valor limite|  Este requerimiento funcional define un rango numerico,por lo que es ideal probar sus extremos y sus bordes  | CP-01, CP-02, CP-03, CP-04, CP-05
| RF2  | Particion de equivalencia | El RF define reglas estructurales sobre el formato del código, lo que genera clases válidas e inválidas claramente diferenciadas      |CP-06, CP-07, CP-08, CP-09, CP-10
| RF3  |  Tabla de desiciones     | El RF combina 3 condiciones independientes (registro, cupos, inscripción previa), lo que genera múltiples combinaciones lógicas que deben cubrirse    |CP-11, CP-12, CP-13, CP-14, CP-15, CP-16, CP-17, CP-18 


## 6. Gestion de Versiones (GitFlow)
