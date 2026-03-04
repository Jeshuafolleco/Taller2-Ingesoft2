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
## Clases de equivalencia

| ID | Descripcion | Rango | Tipo |
|---|---|---|---|
| CE-01 | Por debajo del limite inferior | edad < 16 | Invalida |
| CE-02 | Dentro del rango permitido | 16 <= edad <= 65 | Valida |
| CE-03 | Por encima del limite superior | edad > 65 | Invalida |

---

## Valores limite

| Valor | Descripcion |
|---|---|
| 15 | Justo fuera del rango por abajo |
| 16 | Primer valor valido |
| 40 | Valor representativo del interior |
| 65 | Ultimo valor valido |
| 66 | Justo fuera del rango por arriba |

---

## Casos de prueba

| ID | Clase | Edad ingresada | Resultado esperado | Que se esta probando |
|---|---|---|---|---|
| CP-01 | CE-01 | 15 | Registro rechazado | Limite inferior menos uno |
| CP-02 | CE-02 | 16 | Registro permitido | Limite inferior exacto |
| CP-03 | CE-02 | 40 | Registro permitido | Valor representativo del rango |
| CP-04 | CE-02 | 65 | Registro permitido | Limite superior exacto |
| CP-05 | CE-03 | 66 | Registro rechazado | Limite superior mas uno |
| CP-06 | CE-01 | 0 | Registro rechazado | Valor extremo por abajo |
| CP-07 | CE-03 | 100 | Registro rechazado | Valor extremo por arriba |

---

## Cobertura

| Que se cubre | Casos |
|---|---|
| CE-01 — valores invalidos por abajo | CP-01, CP-06 |
| CE-02 — valores validos | CP-02, CP-03, CP-04 |
| CE-03 — valores invalidos por arriba | CP-05, CP-07 |
| Limite inferior - 1 (15) | CP-01 |
| Limite inferior exacto (16) | CP-02 |
| Limite superior exacto (65) | CP-04 |
| Limite superior + 1 (66) | CP-05 |

Con estos 7 casos de prueba cubrimos el 100% de las clases de equivalencia y todos los valores limite relevantes. Entonces la cobertura ya esta completa.

## 5. Trazabilidad
| Requerimiento  | Tecnica aplicada  |Justificacion|Casos Asociados|
| ------------- |:-------------:|:-------------:|:-------------:|
| RF1  | Analisis de valor limite|  Este requerimiento funcional define un rango numerico,por lo que es ideal probar sus extremos y sus bordes  | CP-01, CP-02, CP-03, CP-04, CP-05
| RF2  | Particion de equivalencia | El RF define reglas estructurales sobre el formato del código, lo que genera clases válidas e inválidas claramente diferenciadas      |CP-06, CP-07, CP-08, CP-09, CP-10
| RF3  |  Tabla de desiciones     | El RF combina 3 condiciones independientes (registro, cupos, inscripción previa), lo que genera múltiples combinaciones lógicas que deben cubrirse    |CP-11, CP-12, CP-13, CP-14, CP-15, CP-16, CP-17, CP-18


## 6. Gestion de Versiones (GitFlow)
