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

## 6. Gestion de Versiones (GitFlow)
