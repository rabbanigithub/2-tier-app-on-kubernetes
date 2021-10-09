# Build Jenkins container
```
docker-compose up -d docker-compose.yml
```
# View the generated administrator password for login
```docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword```

Login using the token, install recommanded plugin and set your password.
