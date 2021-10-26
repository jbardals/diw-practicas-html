# README


## Alcance de la tarea

*  Conocer la estructura de un documento (X)HTML y sus metadatos
* Crear el layout de páginas web estáticas con contenedores genéricos o elementos semánticos
* Usar los elementos HTML adecuados para los distintos tipos de contenidos que se quieran incluir en las páginas HTML


## Pasos previos

### Haz un fork del repositorio original

Haz un fork del repositorio original y **configúralo de forma privada** (la actividad propuesta es individual ;)
Habilita las issues y **otorga permisos de escritura al profesor** en tu repo.  (se te indicará el usuario)


### Clona el repositorio

```
git clone <url de tu fork>
```


### Crea tu rama (personal) de trabajo o *release branch*

Crea tu propia rama de trabajo! Crea esta nueva rama de trabajo a partir de `master`

```bash
# Habitualmente tomará el formato rb-nombreApellido
git checkout -b <rb-usuario>
```

La evolución de tu solución final deberá estar apuntada por esta rama. Puedes utilizar todas las ramas que quieras, pero **no trabajes en la master** y asegúrate, si tienes otras ramas que forman parte de tu solución, de combinarlas (*git merge*) con tu rama con el nombre de tu usuario.



## Revisa periódicamente si se han producido actualizaciones en las especificaciones.

Cada vez que retomes tu trabajo asegúrate tener la última versión de las especificaciones. Para ello:

1. (**Sólo la primera vez**) Añade como repo remoto el repo del profesor desde el que has creado tu fork.

    `git remote add profesor <url-repoProfesor>`

2. (**Cada vez que retomes trabajo**) Revisa novedades y obtenlas del repo del profesor

    `git fetch profesor master`

3. (**Cada vez que haya novedades**) Mezcla estas novedades con tu *release branch*. Si has seguido las indicaciones de este README no deberían producirse conflictos. Si se produjesen adviértelo al profesor.

```bash
    # Asegúrate primero de estar en tu release branch
    git checkout rb-usuario
    
    # Después mézclate en tu rama actual las novedades
    git merge profesor/master
```

## Documenta tu trabajo

El repo debe contener una carpeta nombrada como `doc`. [Sigue las instrucciones](doc/README.md) de cómo documentar.

## Cuándo termines tu trabajo... o eso crees...

### Etiqueta tu versión

Cuando tengas un revisión de tu código que consideres estable, etiquétala de la forma que te indique el [mecanismo de versionado](doc/README.md). Modifica tambien el [changelog](doc/changelog.md) indicando las novedades de la versión.
Puedes hacer etiquetado de tu último commit de la siguiente manera:

```
# Si quieres hacer una etiqueta ligera (solo nombrar un commit
git tag <etiqueta>

# Si quieres hacer una etiqueta que contenga más información
git tag -a <etiqueta> -m 'El mensaje'
```

Si quieres poner una etiqueta a un commit anterior, pon su checksum al final de las instrucciones anteriores.

Recuerda enviar tus tags a tus repos remotos de la siguiente manera:

```
git push <remoto> <tag>
```

Consulta esta [fuente](https://git-scm.com/book/es/v2/Fundamentos-de-Git-Etiquetado) para más detalles.

## Estrategia de ramificación

Rama					| Uso
------------ 			| -------------
`master`	 			| Evolución del enunciado del ejercicio para implementar el juego (enfoque desarrollo con TDD. Contiene tests implementados)
`test-adicionales`      | Partiendo de la rama `master`, se implementan unos test adicionales para aumentar la cobertura del código y probar ciertos aspectos que pudieron obviarse en los primeros tests.
`solucionX`			| Rama que representa una solución (puede derivar de master u otra rama). Tiene implementado tanto el programa como los test unitarios.
`remote\usuario` 	| Evolución de la solución de cada alumno
`remote\teamA..B..C`| Evolución de la solución de cada equipo 


### Changelog de enunciado:

Se irán etiquetando enunciados consolidados y entregados a alumnos. Se dará una explicación general de cada cambio :

Tag				| Descripción
------------ 	| -------------
`enum-v1`		| Enunciado inicial


### Snapshot actual del enunciado en `master`:

```Shell
.
├── README.md
├── doc
│   ├── Demos.md
│   ├── README.md
│   ├── Work.md
│   ├── demo-lidia.gif
│   ├── demo-luis.gif
│   ├── demo-profesor.gif
│   └── nuestrasJavaConventions.xml
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── edu
    │   │       └── xunta
    │   │           └── agrasar
    │   │               └── buscaminas
    │   │                   ├── modelo
    │   │                   │   ├── Buscaminas.java
    │   │                   │   ├── Factoria.java
    │   │                   │   ├── NivelJuego.java
    │   │                   │   └── ReglaBuscaminasException.java
    │   │                   └── vista
    │   │                       ├── App.java
    │   │                       └── VentanaBuscaminas.java
    │   └── resources
    │       └── edu
    │           └── xunta
    │               └── agrasar
    │                   └── buscaminas
    │                       └── vista
    │                           ├── 1.png
    │                           ├── 2.png
    │                           ├── 3.png
    │                           ├── 4.png
    │                           ├── 5.png
    │                           ├── Flag_64.png
    │                           ├── f_Normal_64.png
    │                           ├── f_Ohh_64.png
    │                           ├── f_Smiley_64.png
    │                           ├── f_unhappy_64.png
    │                           ├── minaRota_64.png
    │                           └── mina_64.png
    └── test
        └── java
            └── edu
                └── xunta
                    └── agrasar
                        └── buscaminas
                            └── modelo
                                └── BuscaminasTest.java

23 directories, 28 files
```
