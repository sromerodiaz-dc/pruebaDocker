# Tarea Docker

## 1. Descargar la imagen alpine
```bash
docker pull alpine
```
Descarga la imagen Apine de linux

## 2. Crear contenedor sin nombre
```bash
docker create alpine
docker ps -a
```
Crea un contenedor anonimo y comprueba la existencia del mismo

## 3. Crear contenedor llamado 'dam_alp1'
```bash
docker create --name dam_alp1 alpine
docker start dam_alp1
docker exect -it dam_alp1 sh
```
Crea un contenedor llamado "dam_alp1", se inicia y se accede a el.

## 4. Comprobar IP y ping a google.com
```bash
hostname -I
ping google.com
```
Verifica la IP del contenedor y su conectividad a Internet

## 5. Crear contenedor "dam_alp2" y comprobar conexion con "dam_alp1"
```bash
docker create --name dam_alp2 alpine
docker start dam_alp1 dam_alp2
docker exec -it dam_alp2 sh
ping dam_alp1
```
Crea el contenedor, inicia ambos contenedores, ejecuta dam_alp2 y hace ping a dam_alp1

## Salir del contenedor y ver espacio en disco
```bash
exit
docker system df
```
