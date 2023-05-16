# Clonar este repositorio
git clone https://github.com/oscariquelme01/demo-submodules-fater.git --recursive

# Añadir un submodulo nuevo
`
git submodule add https://github.com/oscariquelme01/demo-submodules-son.git submodules/repo
`

Consideraciones:

- El repo que intentemos añadir como submodulo debe tener al menos un commit
- Git utilizará como rama del submodulo la rama por defecto, 
- Debemos especificar el path, en nuestro caso, probablemente algo como motor/nombre-modulo
- Esto nos 'traera' todo el repositorio de git, puede que nosotros solo estemos interesados en traer el codigo transpilado y minimizado
- Para solucionar esto, podemos escribir un script simple que 'construya' el motor y copiar a una carpeta llamada, por ejemplo, rf-engine y de ahi podemos importar
