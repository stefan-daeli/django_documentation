### Notes
- Already have a project folder
- Use git bash
- Use Windows OS
### Steps
- New environment
```
python -m venv venv
```
- Activate Environment
```
source venv/Scripts/activate
```
- Install Django
```
pip install Django
```
**if installing a specific version:*
```
pip install Django==6.0.1
```
- New Project
```
django-admin startproject config .
```
**config is the name of the project*
- New App
```
python manage.py startapp blog
```
**blog is the name of the app*
- Additional Notes
  - If there is more than one app, it is recommended to create an apps directory to contain all apps.
  ```
  python manage.py startapp blog apps/blog
  ```
  **apps/blog is the directory created before running the command above.*
