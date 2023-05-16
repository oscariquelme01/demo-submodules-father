# Repositorio padre
Este repositorio actuara como el repo padre del ejemplo, en nuestro caso, este repositorio equivale al de un juego.

## Clonar este repositorio
git clone https://github.com/oscariquelme01/demo-submodules-fater.git --recursive

## Añadir un submodulo nuevo
`
git submodule add https://github.com/oscariquelme01/demo-submodules-son.git submodules/repo
`

Consideraciones:

- El repo que intentemos añadir como submodulo debe tener al menos un commit
- Git utilizará como rama del submodulo la rama por defecto, 
- Debemos especificar el path, en nuestro caso, probablemente algo como motor/nombre-modulo
- Esto nos 'traera' todo el repositorio de git, puede que nosotros solo estemos interesados en traer el codigo transpilado y minimizado
- Para solucionar esto, podemos escribir un script simple que 'construya' el motor y copiar a una carpeta llamada, por ejemplo, rf-engine y de ahi podemos importar
- Otra cosa a notar es que al ejecutar este comando, git añadira al staging area el modulo añadido asi como el fichero .gitmodules

### El fichero .gitmodules
- Si es el primer modulo que creamos, git creara un fichero llamado .gitmodules, donde se guardara la informacion sobre los modulos que vayamos añadiendo.
- En este fichero, podremos especificar el path y la rama a usar del modulo entre otras cosas.

Ejemplo de .gitmodules:

```
[submodule "engine/network"]
    path = engine/network
    url = https://bitbucket.com/rfranco/rf-engine-network.git
    branch = branch-example-1

[submodule "engine/reels"]
    path = engine/reels
    url = https://bitbucket.com/rfranco/rf-engine-reels.git
    branch = branch-example-2
```
