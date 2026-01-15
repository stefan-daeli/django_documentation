### Notes
- Already created a Django project
- Already created at least one Django app
- ‘blog’ as an app
### Steps
- Defining apps in the INSTALLED APPS
```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'blog',
]
```
**If the app is in the apps directory (for example), then :*
```
'apps.blog'
```
- Defining templates in the TEMPLATES
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / 'templates'],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
```
**Fill in the value 'DIRS' with this:*
```
[BASE_DIR / ‘templates’]
```
- Databases Configuration (use mysql)
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'blog',
        'USER': 'root',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```
**'blog' is the name of the database*
- STATIC Configuration
```
STATIC_URL = '/static/'
```
**static URL address*
```
STATICFILES_DIRS = [BASE_DIR / 'static']
```
**static source*
