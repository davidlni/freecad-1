# FreeCAD with Netgen and Calculix
## In Docker image Ubuntu Xenial for any Linux 
-----
### FreeCAD 0.17
```
docker pull izone/freecad:0.17
```
```
docker run -ti --rm --name FreeCAD \
--net=host \
-e DISPLAY=unix$DISPLAY \
-v /tmp/.X11-unix \
-v $HOME/.Xauthority:/root/.Xauthority \
izone/freecad:0.17 freecad-daily
```
### FreeCAD 0.16
```
docker pull izone/freecad:0.16
```
```
docker run -ti --rm --name FreeCAD \
--net=host \
-e DISPLAY=unix$DISPLAY \
-v /tmp/.X11-unix \
-v $HOME/.Xauthority:/root/.Xauthority \
izone/freecad:0.16 freecad
```

### Building
```
git clone https://github.com/luvres/freecad.git
cd freecad
```
##### FreeCAD 0.17
```
docker build -t izone/freecad:0.17 ./0.17/
```
##### FreeCAD 0.16
```
docker build -t izone/freecad:0.16 ./0.16/
```
