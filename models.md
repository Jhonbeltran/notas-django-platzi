### Creación de instancia de Modelo usando la Shell de Django
```python
(socialnet) ➜  safepets git:(master) ./manage.py shell                  
Python 3.5.3 (default, Jan 19 2017, 14:11:04)
[GCC 6.3.0 20170118] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> from posts.models import User
>>> fredy = User.objects.create(
...     email='jbeltranleon@gmail.com',
...     password='happypass',
...     first_name='Jhon Fredy',
...     last_name='Beltrán León'
... )
>>> fredy.email
'jbeltranleon@gmail.com'
>>> fredy.pk
1
>>> fredy.id
1
>>> fredy.email = 'jfredybeltran@ucundinamarca.edu.co'
>>> fredy.save()
>>> pablo = User()
>>> pablo.id
>>> #pablo es una instancia pero aun no se almacena en la DB
>>> pablo.email = 'pablo@mail.com'
>>> pablo.password = 'platzi123'
>>> pablo.first_name = 'Pablo'
>>> pablo.last_name = 'Trinidad'
>>> pablo.is_admin = True
>>> pablo.save()
>>> pablo.id
2
>>> pablo.delete()
(1, {'posts.User': 1})

```
