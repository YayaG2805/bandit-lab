## Bandit Level 0
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit1).

**Comandos utilizados:**
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
Explicación:
Se ingresó al servidor por SSH, se listaron los archivos del directorio home y se leyó el archivo readme, que contenía la contraseña del siguiente nivel.

Contraseña obtenida:
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

## Bandit Level 1
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit2).

**Comandos utilizados:**
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls
cat ./-
Explicación:
El archivo que contenía la contraseña tenía como nombre un guion (-). Para evitar que el comando cat lo interpretara como una opción, se usó la ruta relativa ./-.

Contraseña obtenida:
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
## Bandit Level 2
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit3).

**Comandos utilizados:**
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls
cat "./--spaces in this filename--"
Explicación:
El nombre del archivo contenía espacios y comenzaba con guiones (--), lo que hacía que cat lo interpretara como una opción. Para evitarlo, se usó la ruta relativa ./ y se encerró el nombre del archivo entre comillas.

Contraseña obtenida:
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
## Bandit Level 3
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit4).

**Comandos utilizados:**
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls -la
cat ...Hiding-From-You
Explicación:
Se ingresó al directorio inhere y se listaron los archivos. La contraseña estaba en un archivo con nombre “oculto” mediante puntos (...Hiding-From-You), por lo que se leyó directamente con cat.

Contraseña obtenida:
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
## Bandit Level 4
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit5).

**Comandos utilizados:**
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls -la
file ./*
cat ./-file07
Explicación:
Dentro del directorio inhere había múltiples archivos. Usando file ./* se identificó cuál era de tipo texto legible (ASCII). Ese archivo fue -file07, el cual contenía la contraseña.

Contraseña obtenida:
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
## Bandit Level 5
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit6).

**Comandos utilizados:**
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
ls
cd inhere
find . -type f -size 1033c
cat ./maybehere07/.file2
Explicación:
Se buscó dentro de inhere un archivo regular con tamaño exacto de 1033 bytes usando find. El archivo encontrado fue ./maybehere07/.file2 (oculto por el punto inicial), y al leerlo con cat se obtuvo la contraseña.

Contraseña obtenida:
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
## Bandit Level 6
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit7).

**Comandos utilizados:**
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
Explicación:
Se utilizó find (comando incluido en la lista del laboratorio) para buscar en todo el sistema un archivo que cumpliera con: propietario bandit7, grupo bandit6 y tamaño exacto de 33 bytes. Se redirigieron los errores a /dev/null para evitar mensajes de permisos. Luego se leyó el archivo encontrado con cat para obtener la contraseña.

Contraseña obtenida:
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
## Bandit Level 7
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit8).

**Comandos utilizados:**
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
grep millionth data.txt
Explicación:
Se utilizó grep (comando incluido en la lista del laboratorio) para buscar dentro del archivo data.txt la línea que contenía la palabra clave millionth. En esa misma línea se encontraba la contraseña del siguiente nivel.

Contraseña obtenida:
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
## Bandit Level 8
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit9).

**Comandos utilizados:**
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
sort data.txt | uniq -u
Explicación:
Se ordenó el archivo data.txt con sort y luego se utilizó uniq -u para mostrar únicamente la línea que aparece una sola vez. Esa línea correspondía a la contraseña del siguiente nivel. Ambos comandos forman parte de los comandos Unix esenciales solicitados en el laboratorio.

Contraseña obtenida:
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
## Bandit Level 9
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit10).

**Comandos utilizados:**
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
strings data.txt
Explicación:
El archivo data.txt contenía datos con caracteres no imprimibles. Se utilizó strings (comando incluido en la lista del laboratorio) para extraer únicamente las secuencias de texto legible. Dentro de esa salida se identificó la contraseña del siguiente nivel.

Contraseña obtenida:
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
## Bandit Level 10
**Objetivo:**  
Encontrar la contraseña del siguiente nivel (bandit11).

**Comandos utilizados:**
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
ls
cat data.txt
base64 -d data.txt
Explicación:
Se verificó el archivo disponible y se leyó data.txt. Como la información estaba codificada en Base64, se utilizó base64 -d (comando incluido en la lista del laboratorio) para decodificar el contenido y obtener la contraseña del siguiente nivel.

Contraseña obtenida:
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
