## Simple docker build for a bootstrap website
Assuming the ACR name is webacr and it can be found at webacr.azureacr.io. The image will be called webserver.
~~~
az acr login --name webacr
docker build -t webacr.azurecr.io/webserver:latest .
docker push webacr.azurecr.io/webserver:latest
~~~

If you would like to apply multiple tags, like latest and a version #, use the following:

    docker build -t webacr.azurecr.io/webserver:latest -t webacr.azurecr.io/webserver:4.0 .

