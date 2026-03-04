# Documento de Pruebas

## 1. Descripcion del Sistema
Es una aplicación que permite a los estudiantes registrarse y participar en eventos organizados por la universidad. El sistema valida la información ingresada, incluyendo el código estudiantil, antes de permitir la inscripción. Facilita la gestión y control de participantes en cada evento. Garantiza que solo estudiantes con códigos válidos puedan acceder a las actividades.

## 2. Requerimientos a Evaluar
RF - 2 Codigo estudiante

## 3. Tecnicas de Prueba Aplicadas
Particion de equivalencias
La particion de equivalencias es la mejor opción ya que el RF-02 define restricciones con fronteras claras como la longitud, carácter inicial y tipo de caracteres, lo que permite agrupar las entradas en clases donde todos los valores se comportan igual, haciendo innecesario probar cada dato individualmente. Así, en lugar de probar cientos de combinaciones, basta con representar cada clase con un solo caso, logrando máxima cobertura con el mínimo de pruebas posible.

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

## 6. Gestion de Versiones (GitFlow)
