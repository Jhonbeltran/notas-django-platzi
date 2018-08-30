## Creación de un usuario usando la app de auth

```python
>>> from django.contrib.auth.models import User
>>> pau = User.objects.create_user(username='pau', password='happypass')
>>> pau
<User: pau>
>>> pau.id
1
>>> pau.username
'pau'
>>> pau.password
'pbkdf2_sha256$120000$SwQ3PqflNV3P$+uYPLJMQM8WLCRtIuZHn6ZX2FEJCf+rjowSi5UA/Vqw='
```
### Creación de Super-usuario

```bash
(socialnet) ➜  safepets git:(master) ✗ ./manage.py createsuperuser
Username (leave blank to use 'jf'): jbeltranleon
Email address: jbeltranleon@gmail.com
Password:
Password (again):
Superuser created successfully.
```
