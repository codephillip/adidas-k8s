=================
Production test
=================

This contains instructions on how to test the production system on GKE

Tools and Specs
----------------
* GKE cluster - 1
* Nodes(compute engine) - 1(due to high cost): gke-adidasttestcluster-default-pool-28f2aa9d-8hh1 with 2CPUs and 3GB
* Pods - 5(one per service and eventbus)
* Google cloud build. Triggers a build when code is pushed through skaffold or a build pipeline
* Google container registry. Manage Docker images, perform vulnerability analysis
* Google cloud sql - 1: adidas-testdb-instance with 2 CPUs and 4GB
* Google cloud storage. For storing the built images(can be used to store files if need be)

URLS
-------

* Project url is http://www.testadidas.io , however, since no domain has been bought. Run ``minikube ip`` then add the ip address to /etc/hosts with a custom url. Run ``sudo vim /etc/hosts``. Then add ``34.89.53.39 www.testadidas.io``
* Swagger url http://www.testadidas.io/api/v1/swagger

.. note:: All urls but three in swagger require a JWT token. Its best to use postman

* Nats monitoring_. Helps monitor which events services are listening to.(this port is only open for testing purposes)

.. _monitoring: http://34.71.211.38:8222/streaming/clientsz?offset=0&subs=1

Loading postman
~~~~~~~~~~~~~~~~

* Load postman collection by either using this https://www.getpostman.com/collections/b96169c29eb5a9ec6219 or loading the ``Adidas.postman_collection.json`` inside the ``docs`` folder
* Signup with parameters required.
* Sigin with username and password
* Copy ``access`` token and add it to the postman environment variable ``JWT`` or copy paste it manually into the Authorization header as ``JWT eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9foobar``