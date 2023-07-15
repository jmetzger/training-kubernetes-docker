#  

```
# should be at least version 5.9
# as this one includes the yaml.nanorc 
nano --version

# that's it.
echo "include /usr/share/nano/yaml.nanorc" >> /etc/nanorc

# test it
nano test.yml 
```

```
# Step 1: in nano enter 
test:
# <- it works <- colors are there 

# Step 2: Leave nano with keys 
CTRL + x

# Step 3:
# Question from nano: 
# Save modified buffer ?
# Simple press:
n 
```
