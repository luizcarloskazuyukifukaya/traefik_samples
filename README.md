# traefik_samples
Basic samples to understand and confirm the behaver of Traefik 

# References
- https://doc.traefik.io/traefik/user-guides/docker-compose/acme-dns/
- https://doc.traefik.io/traefik/https/acme/#providers
- https://doc.traefik.io/traefik/getting-started/configuration-overview/
- https://www.youtube.com/watch?v=tgh6mKj2yEw&list=PLuvRKxeqrv4JxyDhH4yhDoYHuFnWQGEzI&index=4

# Quick Start
## Select Target Domain Namage Management Service
1. Move to the folder representing the target DNS Management Service
For example, for Duck DNS, move to duckdns.org directory

2. Update the Token stored on ./secrets directory

3. For Staging or Production, you may need to specify target in the Traefik.yml file.

4. Launch Docker Container
- docker ps
- docker compose stop ; docker compose rm -f
- rm letsencrypt/acme.json
- touch letsencrypt/acme.json
- chmod 0600 letsencrypt/acme.json 
- docker compose up -d
- docker logs traefik

