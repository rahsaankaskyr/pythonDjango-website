Learning and making a basic Python website with Django framework.


python hello.py runserver

http://127.0.0.1:8000/hello/


Django code explanation:
The top lines import the Django library:

from django.conf import settings 
from django.conf.urls import patterns
from django.http import HttpResponse
from django.core.management import execute_from_command_line



If you open the link /hello/, the webserver will call the index() function. We map the url to the function using:

urlpatterns = patterns('',
    (r'^hello/$', index),
)

In Django we have url friendly urls. This means you do not have a url that ends in /id=1359835, but instead we have the directory as name.  Finally, we set some default settings using settings.configure.