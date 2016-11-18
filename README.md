# django-rest-framework-email-accounts
**django-rest-framework-email-accounts** is a simple Django app for django-rest-framework that use email instead of username to identify users.

## Quick start

1. Before using this app you must install django-rest-framework with:

    ```shell
    pip install djangorestframework
    ```
   and django-rest-framework-jwt with:
    
    ```shell
    pip install djangorestframework-jwt
    ```

2. Add "django-rest-framework-email-accounts" to your INSTALLED_APPS setting like this:

    ```python
    INSTALLED_APPS = [
        ...
        'rest_framework',
        'django-rest-framework-email-accounts',
    ]
    ```

3. Include the django-rest-framework-email-accounts URLconf in your project urls.py like this:

    ```python
    url(r'^accounts/', include('django-rest-framework-email-accounts.urls')),
    ```

4. Run `python manage.py migrate` to create the django-rest-framework-email-accounts models.

5. Start the development server and visit http://127.0.0.1:8000/admin/
   to create a django-rest-framework-email-accounts (you'll need the Admin app enabled).

6. The available urls are:
    * *https://127.0.0.1:8000/accounts/users/* for creating a new user with POST request
    * *https://127.0.0.1:8000/accounts/token-auth/* for obtaining token
    * *https://127.0.0.1:8000/accounts/token-refresh/* for refreshing token
    * *https://127.0.0.1:8000/accounts/token-verify/* for verifying token
