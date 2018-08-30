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
```
