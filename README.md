# Attention
    - The ssh keys inside the 'ssh' directory are for test use only for this project, do not reuse these keys in other projects as they are open for public viewing.


To run this program you will need the docker (20.10.12, build e91ed57) and docker compose (v2.2.3).

How to run:

Run 'docker-compose up -d' in your terminal to up your dockers (inside the main folder 'tema11').
Run 'docker exec -it ansible bash' to enter in main docker.
Run 'cd ansible' to enter in ansible directory.
Run 'ansible-playbook playbook.yml' to run automatized environment.

That command sequence will make the microservice run automatically.

Microservice informations:

All endpoints is present and explained in default localhost page.

To access default localhost page, input this ip in your browser after start the docker image/container: http://localhost:8080 or http://127.0.0.1:8080
