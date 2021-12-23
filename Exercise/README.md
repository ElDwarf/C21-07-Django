# Ejemplo 01

Basando el repositorio del ejercicio anterior o en el del ejemplo ((Repo)[https://github.com/ElDwarf/django-examples]), implementar los siguientes cambios.


## Paso 1. Crear un branch en el repositorio.


## Paso 2. Mirar los html a templates


1. Crear template base con el html siguiente HTML

```html
{% load static %}
<!DOCTYPE html>
<html>
    <body>
        <h1>{{ title }} {{ request.user.first_name | title }}</h1>
        <hr>
        {% block content %}
        {% endblock %}
        {% comment %}
        <br>
        {{ now|date:"d/m/Y h:m" }}
        <br>
        {{ name }}
        <img |src="{% static 'img/640px-Python-logo-notext.svg.png' %}" height="80px" width="80px"/>
        {% endcomment %}
    </body>
</html>
```

2. Mirar html de las vistas a los templates nuevos basandose en el html base.html

## Paso 3. Agregar configuracion de archivos estaticos y probarlos.

## Paso 4. Incorporar model form y procesar desde la lista de alumnos el formularios


form.py
```py
from django.forms import ModelForm

from .models import Alumno


class AlumnoForm(ModelForm):
    class Meta:
        model = Alumno
        fields = ['first_name', 'last_name', 'curso', 'birthday']
```

