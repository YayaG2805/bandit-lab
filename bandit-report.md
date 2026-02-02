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
