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

--

### Notas Clase 2

#### Conceptos del Modelo Relacional

- El modelo relacional representa datos como **tablas bidimensionales** llamadas relaciones
- Elementos principales:
    - **Relaciones (tablas)**: Estructuras bidimensionales que almacenan datos
    - **Atributos**: Columnas de las tablas que representan propiedades
    - **Esquema**: Nombre de la relación + conjunto de atributos (sin orden preestablecido)
    - **Tuplas**: Filas de cada relación que contienen valores concretos
    - **Dominio**: Cada componente debe ser atómico (no compuesto)
    - **Clave**: Conjunto de atributos que no permite valores repetidos

#### Reglas de Transformación 1 a 1 (E-R a Relacional)

- Transformación de entidades:
    - Crear una relación con el mismo nombre y atributos
    - La clave en el modelo relacional corresponde al identificador de la entidad
- Transformación de relaciones:
    - Crear una relación con el mismo nombre
    - Incluir como atributos los identificadores de las entidades participantes
    - Agregar los atributos propios de la relación
    - La clave depende de la cardinalidad

#### Casos Especiales de Transformación

- **Relaciones con roles**: Renombrar atributos cuando una entidad participa más de una vez
    - Ejemplo: Empleado-Director donde se renombra "número de empleado" a "número de director"
- **Generalización**: Tres opciones de transformación
    1. Solo transformar la entidad de nivel superior (agregando atributo discriminante)
    2. Solo transformar las entidades de nivel inferior (repitiendo atributos comunes)
    3. Transformar todas las entidades (nivel superior e inferior)
- **Especialización**: Dos opciones de transformación
    1. Solo transformar la entidad de nivel superior (con atributo discriminante)
    2. Transformar todas las entidades (nivel superior e inferior)
- **Agregación**: Transformar entidades y relaciones participantes, y la relación con la agregación

#### Actividades para la próxima clase

- [ ]  Interpretar el modelo de entidades y relaciones presentado
- [ ]  Redactar la semántica del modelo en lenguaje coloquial
- [ ]  Aplicar las reglas para transformar el modelo E-R al modelo relacional
- [ ]  Subir consultas al foro sobre el contenido de la clase