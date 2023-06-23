# Working with permissions with bind-mount  (Rocky with SELinux)

## Step: 1

```
sestatus
docker run --rm -it --mount type=bind,source=/home/kurs/nginx/html,target=/usr/share/nginx/html --name=nginx-test nginx bash
```
