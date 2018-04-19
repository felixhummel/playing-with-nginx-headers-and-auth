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
curl -v http://localhost/a
```
