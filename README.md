# Nginx: Map Cookie to Proxy Header

Three shells:
```
# logs
docker-compose up -d && docker-compose logs -f

# reloader
docker-compose exec nginx sh -c 'while true; do nginx -s reload; sleep 3; done'

# client
watch -n1 curl -s --cookie-jar /tmp/foojar --cookie @/tmp/foojar http://foo.example.org/
```

# Auth Headers
```
# check /auth works
curl -v http://localhost/a

# pass stuff from /auth to echo
curl -v localhost/ah
```
