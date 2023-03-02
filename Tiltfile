#Tiltfile

docker_compose('docker-compose.yml')

backend = {
    "newsletter-microservice": "http://localhost:420/",
    "users-microservice": "http://localhost:1017/"
}

frontend = ["ui-starter-app"]

def register_backend():
    print('registering backend services')
    for service in backend:
        dc_resource("{}".format(service), labels=["back_end"])
    print('registered backend services')

register_backend()

def register_frontend():
    for service in frontend:
        dc_resource("{}".format(service), labels=["front_end"])

register_frontend()