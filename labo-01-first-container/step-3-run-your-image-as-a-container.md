# Step 3 - Run your image as a container

* [Official Source](https://docs.docker.com/language/java/run-containers/)

<!---->

* [ ] Run your "petclinic" docker based on the image created in the previous step.
  * [ ] We should access to your application using the http standard port.

Result expected:

{% hint style="info" %}
Linux user, change ^ by ' to execute multi lines commands.
{% endhint %}

```
[INPUT]
curl --request GET ^
--url http://localhost/actuator/health ^
--header 'content-type: application/json'

[OUTPUT]
{"status":"UP"}

//disregard the message curl: (6) Could not resolve host: application
```

* [ ] List all Dockers currently running on your local environment. Observe the port forwarding for your "petclinic" docker.

```
[INPUT]
docker ps

[OUTPUT]
CONTAINER ID   IMAGE                              COMMAND                  CREATED         STATUS         PORTS     NAMES
cfab789d305d   eclipse-petclinic:version1.0.dev   "./mvnw spring-boot:…"   2 minutes ago   Up 2 minutes             compassionate_mccarthy

```

* [ ] Stop your "petclinic" docker

```
[INPUT]
docker stop <CONTAINER ID>

[OUTPUT]
Stop the container
```

* [ ] Rename your docker as "petclinic-app"

<!---->

* [Official doc](https://docs.docker.com/engine/reference/commandline/rename/)

```
[INPUT]
docker tag eclipse-petclinic:version1.0.dev petclinic-app:version1.0.dev

[OUTPUT]
docker image
REPOSITORY          TAG              IMAGE ID       CREATED          SIZE
petclinic-app       version1.0.dev   7df82d1f61e2   22 minutes ago   607MB
```

* [ ] Restart your docker using the new name

```
[INPUT]
docker restart petclinic-app

[OUTPUT]
the docker is restarting
```

* [ ] Display all running dockers with this output format

<!---->

* [Official doc](https://docs.docker.com/config/formatting/)

Result expected:

```
IMAGE                              PORTS.                  NAMES
eclipse-petclinic:version1.0.dev   0.0.0.0:80->8080/tcp.   petclinic-server
```

```
[INPUT]
docker ps --format "table {{.Image}}\t{{.Ports}}\t{{.Names}}"


[OUTPUT]
IMAGE                          PORTS     NAMES
petclinic-app:version1.0.dev             petclinic_app_dev
```

