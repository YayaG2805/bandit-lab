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
