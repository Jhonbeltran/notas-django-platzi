### Consultas

```python
>>> from posts.models import User
>>> #Consultar un usuario
>>> user = User.objects.get(email='freddier@platzi.com')
>>> user.pk
8
>>> user.first_name
'Freddy'
```

### Usaremos el `__` para indicar el uso de una consulta especial
```python
>>> platzi_users = User.objects.filter(email__endswith='@platzi.com')
>>> platzi_users
<QuerySet [<User: User object (7)>, <User: User object (8)>, <User: User object (9)>, <User: User object (10)>]>
```
### Usando la función `__str__` en el modelo obtenemos
```python
>>> platzi_users
<QuerySet [<User: cvander@platzi.com>, <User: freddier@platzi.com>, <User: yesica@platzi.com>, <User: arturo@platzi.com>]>
```

### Usamos `all` para seleccionar todos los elementos

```python
>>> users = User.objects.all()
>>> users
<QuerySet [<User: cvander@platzi.com>, <User: freddier@platzi.com>, <User: yesica@platzi.com>, <User: arturo@platzi.com>, <User: jbeltranleon@gmail.com>]>
```

### Actualizar multiples registros

```python
>>> platzi_users = User.objects.filter(email__endswith='@platzi.com').update(is_admin=True)
>>> platzi_users
4
```

https://docs.djangoproject.com/en/2.0/topics/db/queries/
