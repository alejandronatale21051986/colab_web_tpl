#INFO: web en gitpages usando cuadernos de Colab

La barra de navegación, footer, etc. se pueden modificar desde la plantilla `tpl/index.html.j2' 

Para publicar una página nueva o actualizar desde el menú de Google Colab elegí "Guardar en Github" y la rama `main` de este repositorio.

Un script de github actions genera html usando los cuadernos y lo publica en gitpages, se puede ver en `.github/workflows/ipynb_to_html.yml`

Si querés hacer lo mismo localmente podés ejecutar los comandos que vés en ese script. En particular

```
pip install jupyter nbconvert #U: instalar, una sola vez
jupyter nbconvert -y --output-dir=./_build/html --to html --template=tpl --theme=dark *.ipynb
```
 

