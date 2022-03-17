# django-getting-started

1) Download and install python 3 from https://www.python.org/
2) Create a virtual environment (https://peps.python.org/pep-0405/) and activate the same
3) Install Django within the virtual environment
4) On the command prompt run, 
  4.1) "django-admin startproject mysite" to create a project
  4.2) "python manage.py runserver" to run the django webserver
5) On your browser, visit "http://127.0.0.1:8000/" to access the site
6) On command prompt run,
  6.1) "python manage.py startapp polls" to create the app
7) In an editor, open "polls/views.py", add the below snippet and save,
        from django.http import HttpResponse
        def index(request):
            return HttpResponse("Hello, world. You're at the polls index.")
8) Create "urls.py" within "polls" app folder in an editor, add the below snippet and save,
        from django.urls import path
        from . import views
        urlpatterns = [path('', views.index, name='index'),]
9) In an editor, open "mysite/urls.py", add the below snippet and save,
        from django.contrib import admin
        from django.urls import include, path
        urlpatterns = [
            path('polls/', include('polls.urls')),
            path('admin/', admin.site.urls), ]
10) On command prompt run, "python manage.py runserver" to run the django webserver
11) On your browser, visit "http://127.0.0.1:8000/" to access the site
12) If you get an error page, check that you’re going to http://localhost:8000/polls/ and not http://localhost:8000/

HAPPY LEARNING!

Source:  https://docs.djangoproject.com/en/4.0/intro/tutorial01/
