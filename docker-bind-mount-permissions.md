# Working with permissions with bind-mount  (Rocky with SELinux)

## Step: 1

```
# als unpriviligierter Nutzer kurs 
cd
mkdir -p /home/kurs/nginx/html 
cd /home/kurs/nginx/html
echo "hallo welt" > index.html 
sestatus
docker run --rm -it --mount type=bind,source=/home/kurs/nginx/html,target=/usr/share/nginx/html --name=nginx-test nginx bash
```
