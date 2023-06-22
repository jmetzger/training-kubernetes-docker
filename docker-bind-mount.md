# Working with bind-mount


## Example 1 

```
# andere Verzeichnis als das Heimatverzeichnis von root funktionieren aktuell nicht mit 
# snap install docker 
# wg. des Confinements 
docker run -d -it  --name devtest --mount type=bind,source=/root,target=/app nginx:latest
docker exec -it devtest bash 
/# cd /app 
```

## Example 2 with /home/kurs 

```
# testen wo der DocumentRoot 
docker run --rm -p 80:80 -it --name=nginx-test nginx bash 

```
