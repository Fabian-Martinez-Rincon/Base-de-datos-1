# Base-de-datos-1

Creamos el entorno

```
python -m venv venv
```
Activamos el entorno

```
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass; .\venv\Scripts\Activate
```

Instalamos las dependencias

```
pip install -r requirements.txt
```

Iniciamos Jupyter Lab

```
jupyter lab
```

---

### Notas Clase 1

#### Introducción a Modelos de Datos

- Un modelo de datos provee una notación para describir datos mediante tres elementos:
    - Estructura de los datos
    - Restricciones que aplican sobre los datos
    - Operaciones que pueden realizarse sobre los datos
- Los modelos de datos constituyen la estructura subyacente de una base de datos
- Clasificación de modelos:
    - Modelos lógicos: basados en objetos (entidad-relación, orientado a objetos) y basados en registros (relacional)
    - Modelos no lógicos

#### Modelo Entidad-Relación

- Es un modelo lógico basado en objetos que representa el significado de los datos independientemente de su implementación física
- Componentes estructurales:
    - Entidades: objetos distinguibles (ejemplos: persona, auto)
    - Relaciones: asociaciones entre entidades (ejemplo: "es dueño de")
    - Atributos: información sobre entidades o relaciones
    - Dominio: conjunto de valores posibles para un atributo
    - Rol: función que cumple una entidad en una relación
- Representación gráfica:
    - Rectángulos para entidades
    - Rombos para relaciones
    - Círculos para atributos (rellenos si son identificadores)
    - Líneas con notaciones para cardinalidad

#### Restricciones del Modelo

- Cardinalidad: indica cuántas veces una entidad puede participar en una relación (1:1, 1:N, N:M)
- Identificadores/claves: atributos que identifican de forma única a una entidad
    - Pueden ser simples o compuestos
    - Solo las entidades pueden tener atributos identificadores

#### Modelo Entidad-Relación Extendido

- Especialización: definir subconjuntos de entidades (ejemplo: empleados → médicos)
- Generalización: proceso inverso a la especialización, creando entidades de nivel superior
- Agregación: mecanismo para tratar una relación como una entidad de alto nivel
    - Útil cuando se necesita relacionar información con una relación existente
    - Ejemplo: relacionar entrevistas (relación entre compañía y solicitante) con ofertas de empleo

#### Estructura del Curso

- Los materiales presentados son solo un resumen de los conceptos
- Estudiantes deben consultar la bibliografía para profundizar
- Se espera participación activa: