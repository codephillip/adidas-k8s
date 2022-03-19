===========================
Adidas test Documentation
===========================

Introduction
============

This is the adidas backend challenge


Tools
-------

#. Typescript: Used to enforce data types mostly in asynchronous communication
#. Swagger: Used for documentation
#. Postman: Used to test various endpoints and create documentation
#. Expressjs: Used to run microservices using Javascript
#. Kubernetes: Used to manage microservice deployment, scaling and monitoring
#. Docker: Used to encapsulate each service for easy deployment
#. NATS: Used as an event bus in asynchronous communication
#. Skaffold: Used for quick testing and running k8s commands
#. Minikube: Used to run k8s on dev environment
#. kubectl: Used to manage k8s resources
#. kubectx: Used to change between k8s contexts ie minikube, gke_foobar
#. MongoDB: Used for storage of temporary and less consistent data
#. PostgresDB: Used for storage of more permanent and consistent data
#. CommonLibrary: Used to share commonly reused components between services
#. reStructuredText(rst): Used to write the docs
#. Markdown: Used to write short docs in the README.md
#. Django: Used to create web microservice(only authentication service)
#. Django Rest Framework: Used to create REST api endpoints in Django
#. Python3: Used to implement the programming logic in Django microservices
#. GCP: Used to build and run the k8s production app

Microservices
---------------

- adidas-express-public. A backend for frontend service that acts a proxy server. Handles authentication, DDOS attacks
- adidas-express-sub. Allows users to subscribe to a newsletter or campaign(one public url, the rest are admin access only)
- adidas-express-email. Allows admins to send emails to the users(admin access only)
- adidas-django-auth. An authentication service written in django and generates JWT tokens

Resources
-----------

* Kubernetes cheetsheet_
* Kubectl `docs or book`_
* Microservices course_
* Kubernetes_ course
* Microservices article_ that covers; Django, k8s, Docker, Celery, Redis, AWS, Postgres, Prometheus, etc.
* Microservices patterns with Java by Richardson_
* Microservices: `Up and Running`_ by Ronnie Mitra
* `Building Microservices`_ by Sam Newman
* Architecting container and microservice-based applications_ microsoft
* Microsoft .Net `architecture blog`_
* .NET Microservices: Architecture for Containerized_ .NET Applications
* Sphinx_ reStructuredText docs
* Sourceforge_ reStructuredText docs
* `Nats demo`_
* `Nats JS docs`_
* `Nats python docs`_
* `Nats parameters and docs`_
* `k8s best practises`_
* `My blog post`_


.. _cheetsheet: https://kubernetes.io/docs/reference/kubectl/cheatsheet/
.. _docs or book: https://kubectl.docs.kubernetes.io/guides/
.. _course: https://www.udemy.com/course/microservices-with-node-js-and-react/
.. _article: https://markgituma.medium.com/kubernetes-local-to-production-with-django-1-introduction-d73adc9ce4b4
.. _Richardson: https://www.amazon.com/Microservices-Patterns-examples-Chris-Richardson/dp/1617294543
.. _microservices: https://dzone.com/articles/design-patterns-for-microservices
.. _Kubernetes: https://www.udemy.com/course/kubernetes-made-easy
.. _Sphinx: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Sourceforge: https://docutils.sourceforge.io/docs/user/rst/quickref.html
.. _Nats demo: https://github.com/codephillip/nats-streaming-server-nodejs-demo
.. _Nats JS docs: https://github.com/nats-io/stan.js
.. _Nats python docs: https://github.com/nats-io/stan.py
.. _Nats parameters and docs: https://hub.docker.com/_/nats-streaming
.. _k8s best practises: https://www.youtube.com/playlist?list=PLIivdWyY5sqL3xfXz5xJvwzFW_tlQB_GB
.. _kubectx: https://github.com/ahmetb/kubectx
.. _Up and Running: https://www.oreilly.com/library/view/microservices-up-and/9781492075448/
.. _My blog post: https://medium.com/dev-scribbles
.. _Building Microservices: https://samnewman.io/books/building_microservices_2nd_edition/
.. _applications: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/#container-design-principles
.. _Containerized: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/


Setup pages
============

:Setup instructions:
:doc:`Setup instructions </setup>`

:More:
:doc:`More </other>`

:Production test:
:doc:`Production test </productiontest>`