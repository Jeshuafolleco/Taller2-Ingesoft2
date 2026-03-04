# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar
RF-01 Registro de Estudiante (Edad)

## 3. Tecnicas de Prueba Aplicadas
Escogí dos tecnicas combinadas:

- **Particion de Equivalencia (PE)**
- **Analisis de Valores Limite (AVL)**
Porque el requerimiento trata de un rango numerico, y estas dos tecnicas son las que mejor se ajustan a ese tipo de condicion.

Con la **Particion de Equivalencia** se agrupan los valores que el sistema trata igual, lo que permite reducir la cantidad de pruebas sin perder cobertura. En este caso hay tres grupos: valores por debajo del rango, dentro del rango y por encima.

Con el **Analisis de Valores Limite** se prueban los bordes exactos del rango, porque ahi es donde suelen aparecer los errores (por ejemplo, usar < en vez de <=). Probar 15, 16, 65 y 66 cubre esos puntos criticos.

## 4. Casos de Prueba Diseñados

## 5. Trazabilidad
| Requerimiento  | Tecnica aplicada  |Justificacion|Casos Asociados|
| ------------- |:-------------:|:-------------:|:-------------:|
| RF1  | Analisis de valor limite|  Este requerimiento funcional define un rango numerico,por lo que es ideal probar sus extremos y sus bordes  | CP-01, CP-02, CP-03, CP-04, CP-05
| RF2  | Particion de equivalencia | El RF define reglas estructurales sobre el formato del código, lo que genera clases válidas e inválidas claramente diferenciadas      |CP-06, CP-07, CP-08, CP-09, CP-10
| RF3  |  Tabla de desiciones     | El RF combina 3 condiciones independientes (registro, cupos, inscripción previa), lo que genera múltiples combinaciones lógicas que deben cubrirse    |CP-11, CP-12, CP-13, CP-14, CP-15, CP-16, CP-17, CP-18 


## 6. Gestion de Versiones (GitFlow)
