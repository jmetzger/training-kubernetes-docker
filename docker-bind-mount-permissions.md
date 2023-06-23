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
exit
```

## Step: 2

```
# Adjust permissions 
cd /home/kurs/nginx/
sudo chown -R kurs:kurs html
# Neue Verzeichnisse und Dateien werden mit der Gruppe kurs angelegt
chmod -R g+s html
setfacl -d -m g::rwx html
docker run --rm -it --mount type=bind,source=/home/kurs/nginx/html,target=/usr/share/nginx/html --name=nginx-test nginx bash
# in container
cd /usr/share/nginx/html
mkdir rootdata
cd rootdata
touch foo

```
