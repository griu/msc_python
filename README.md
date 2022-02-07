
# ANEXO: README DE PYTHON

## PREPARACIÓN DEL ENTORNO COLAB

Des de [Colab](http://colab.research.google.com), hay que clonar el repositorio y preprar el entorno, cada vez que inicias un nuevo libro. En los libros se incluye el código necesario.

```
if 'google.colab' in str(get_ipython()):
    !git clone https://github.com/griu/msc_python.git /content/msc_python
    !git -C /content/msc_python pull
    %cd /content/msc_python
```

## PREPARACIÓN ENTORNO LOCAL-JUPYTER (OPCIONAL)

### CLONAR EL PROYETO GITHUB EN LOCAL

Abrimos una línea de comandos (`cmd` o `anaconda` en Windows, `terminal` en Linux).

```
git clone https://github.com/griu/msc_python.git
```

Para actualizarlo de nuevo, des de consola.

```
cd msc_python
git pull
```

### CREAR EN LOCAL UN NUEVO ENVIRONMENT DE ANACONDA

Abrimos una línea de comandos (con *Anaconda 3.0* ya disponible).

- Windows: Escribimos `Anaconda` en el menú Inicio y aparecerá la consola MS-DOS de Anaconda.
- Linux: Abrimos Terminal

```
conda deactivate
conda create -n msc_python python=3.6.9
conda activate msc_python
```

Verifica que se ha creado y está activo.

```
conda info --envs
```

### INSTALA LAS LIBRERIAS DE PYTHON

```
cd msc_python
conda activate msc_python
python -m pip install -r requirementsColab.txt
```

### PUBLICAR EL KERNEL

Para acceder al nuevo environment desde Jupyter necesitas publicar el kernel.

```
python -m ipykernel install --user --name msc_python --display-name "msc_python"
```

Puede tardar unos minutos en publicarse.

### LANZAR ENTORNO JUPYTER NOTEBOOK

Para acceder al servidor Jupyter. 

```
conda activate msc_python
jupyter notebook
```

Debería abrirse un navegador con acceso a Jupyter desde donde podrás acceder a los notebooks.  Habitualmente el servidor Jupyter se abre en http://localhost:8888/ .

