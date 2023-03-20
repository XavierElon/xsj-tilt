#Tiltfile

docker_compose('docker-compose.yml')

backend = {
    "newsletter-microservice": "http://localhost:420/",
    "users-microservice": "http://localhost:1017/",
    "deno-microservice": "http://localhost:4200/"
}

frontend = {
    "ui-starter-app": "http://localhost:3000/",
    "xsj-consulting-app": "http://localhost:4269/",
    "xsj-reusable-component-library": "http://localhost:6006/"
}

def register_backend():
    for service in backend:
        dc_resource("{}".format(service), labels=["back_end"])

register_backend()

def register_frontend():
    for service in frontend:
        dc_resource("{}".format(service), labels=["front_end"])

register_frontend()
