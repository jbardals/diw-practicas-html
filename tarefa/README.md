# README


## Alcance de la tarea

*  Conocer la estructura de un documento (X)HTML y sus metadatos
* Crear el layout de páginas web estáticas con contenedores genéricos o elementos semánticos
* Usar los elementos HTML adecuados para los distintos tipos de contenidos que se quieran incluir en las páginas HTML


## Pasos previos

### Haz un fork del repositorio original

Haz un fork del repositorio original
Habilita las issues y **otorga permisos de escritura al profesor** (usuario **bardal**) en tu repo.


### Clona el repositorio

```
git clone <url de tu fork>
```


### Crea tu rama (personal) de trabajo o *release branch*

Crea tu propia rama de trabajo! Crea esta nueva rama de trabajo a partir de `main`

```bash
# Habitualmente tomará el formato rb-nombreApellido
git checkout -b <rb-usuario>
```

La evolución de tu solución final deberá estar apuntada por esta rama. Puedes utilizar todas las ramas que quieras, pero **no trabajes en la main** y asegúrate, si tienes otras ramas que forman parte de tu solución, de combinarlas (*git merge*) con tu rama con el nombre de tu usuario.



## Revisa periódicamente si se han producido actualizaciones en remoto

Cada vez que retomes tu trabajo asegúrate tener la última versión de las especificaciones. Para ello:

1. (**Sólo la primera vez**) Añade como repo remoto el repo del profesor desde el que has creado tu fork.

    `git remote add profesor <url-repoProfesor>`

2. (**Cada vez que retomes trabajo**) Revisa novedades y obtenlas del repo del profesor

    `git fetch profesor main`

3. (**Cada vez que haya novedades**) Mezcla estas novedades con tu *release branch*. Si has seguido las indicaciones de este README no deberían producirse conflictos. Si se produjesen adviértelo al profesor.

```bash
    # Asegúrate primero de estar en tu release branch
    git checkout rb-usuario
    
    # Después mézclate en tu rama actual las novedades
    git merge profesor/main
```

## Para entregar la tarea

En la carpeta **tarefa** debes crear una carpeta para cada ejercicio de la tarea.
En la carpeta de cada ejercicio deberás entregar todos los ficheros necesarios para ese ejercicio y 
organizados de la siguiente manera:
* Guarda las imágenes en una carpeta `img/` (se recomienda formatos menos pesados como PNG)
* Guarda las hojas de estilo en en una carpeta `css/`
* Guarda los ficheros de javascript en en una carpeta `js/`


### Etiqueta tu versión

Cuando tengas un revisión de tu código que consideres estable, etiquétala de la siguiente forma:

```
git tag html-v1.0-pacoPerez
```

* html-v1.x-nombreApellido1 donde x representa un número secuencial en cada incremento

Puedes hacer etiquetado de tu último commit de la siguiente manera:

```
# Si quieres hacer una etiqueta ligera (solo nombrar un commit)
git tag <etiqueta>

# Si quieres hacer una etiqueta que contenga más información
git tag -a <etiqueta> -m 'El mensaje que quieras'
```
### Envía tus tags a tus repos remotos:
```
git push <remoto> <tag>
```

## Ramas

Rama					| Uso
------------ 			| -------------
`main`	 			| Contenidos suministrados por el profesor
`remote\usuario` 	| Evolución de la solución de cada alumno


![Enunciado de la Tarea](enunciado.md)
