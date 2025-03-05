# apso-apuntes-practica2

## 📂 1. Creación y Gestión de Directorios y Archivos

🔹 **Crear directorios** usando `mkdir` con la opción `-p` para estructuras anidadas:
```sh
mkdir -p prac2/prac21/tmp1 prac2/prac22 prac2/prac23/tmp2
```

🔹 **Cambiar de directorio** con `cd` (rutas absolutas y relativas):
```sh
cd /home/velez/prac2  # Ruta absoluta
cd ModuloI/Practica1/ # Ruta relativa
```

🔹 **Copiar y mover archivos:**
```sh
cp /home/so/velez/MI/f[12].txt .   # Copiar archivos con patrón
mv tmp1/f1.txt tmp1/f21.txt         # Renombrar archivo
mv tmp1/f2.txt ../prac23/tmp2/f23.txt  # Mover y renombrar en un paso
```

---

## 🔐 2. Gestión de Permisos

🔹 **Modificar permisos con `chmod`**

- 🔹 Notación simbólica:
```sh
chmod og-rw .  # Quitar permisos de lectura y escritura a grupo y otros
```
- 🔹 Notación numérica:
```sh
chmod 740 f1.txt f2.txt  # Propietario: rwx, Grupo: r, Otros: sin permisos
chmod 700 ../Practica2    # Propietario: rwx, sin permisos para otros
```

---

## 🔍 3. Búsqueda de Archivos y Directorios

🔹 **Buscar directorios con `find`**
```sh
find /home/velez -type d -name "?[rRtT]*[!0-9][0-9]"
```

🔹 **Buscar archivos modificados en los últimos 100 días:**
```sh
find /etc -type f -mtime -100
```

---

## 📑 4. Uso de `grep`, `wc`, `sort`, `head` y `tail`

🔹 **Buscar contenido en archivos con `grep`**
```sh
grep -i "llama" ../../f1.txt ../../f2.txt  # Ignora mayúsculas/minúsculas
grep -i 'Cobi' versos
```

🔹 **Contar caracteres y líneas con `wc`**
```sh
wc -c group    # Número de caracteres
twc -L passwd  # Longitud de la línea más larga
```

🔹 **Ordenar archivos con `sort`**
```sh
sort group          # Orden ascendente
sort -r group       # Orden descendente (inverso)
```

🔹 **Mostrar primeras y últimas líneas de un archivo**
```sh
head -3 passwd   # Primeras 3 líneas
tail -3 passwd   # Últimas 3 líneas
```

---

## 📅 5. Fecha, Hora y Calendario

🔹 **Mostrar calendario de un mes y año específicos:**
```sh
cal 7 1993  # Ver mes de julio de 1993
cal 1 2022  # Ver enero de 2022
```

🔹 **Mostrar fecha y hora con formato personalizado:**
```sh
date +"Año: %Y, Mes: %m, Día: %d"
date +"Bienvenido. Son las %H horas y %M minutos del %A %e de %B. Ha sido un placer"
```

---

## 🔗 6. Enlaces (Hard Links y Soft Links)

🔹 **Crear un enlace duro:**
```sh
ln /home/velez/prac1/solp1.txt solucionprac1
```

🔹 **Crear un enlace simbólico:**
```sh
ln -s prac23/tmp2 temporal
ln -s ../Practica1/Datos/fichcancion versos
```

🔹 **Verificar el tipo de enlace:**
```sh
file solucionprac1 temporal
```

---

## ⚙️ 7. Gestión de Procesos y Usuarios

🔹 **Ver usuarios conectados:**
```sh
who -q   # Muestra nombres y número de sesiones
who -H   # Incluye cabecera
```

🔹 **Ver procesos y monitorizar el sistema:**
```sh
ps -u velez   # Listar procesos del usuario
top           # Ver procesos en tiempo real
```

🔹 **Finalizar procesos:**
```sh
kill -9 <pid-proceso>  # Forzar la finalización de un proceso
```

🔹 **Consultar información de usuario y terminal:**
```sh
id -g   # Ver ID de grupo
tty     # Ver terminal en uso
```

🔹 **Enviar mensajes a otros usuarios con `write`**
```sh
write <usuario> <tty>
# Escribir mensaje y finalizar con CTRL + d
```

🔹 **Control de recepción de mensajes:**
```sh
mesg n  # Bloquear mensajes
mesg y  # Permitir mensajes
```

---

## 📌 8. Otros Comandos y Consejos

🔹 **Visualizar archivos:**
```sh
more prac2/f1.txt  # Leer archivos de forma paginada
```

🔹 **Diferencia entre rutas absolutas y relativas:**
- **Ruta absoluta:** `/home/usuario/...`
- **Ruta relativa:** `../Practica2`

🔹 **Salir del sistema correctamente:**
```sh
exit
```

---
