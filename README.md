# Tarea 1: Sistema de Tickets 

Este programa simula un sistema básico de atención técnica. Permite registrar, buscar y atender tickets con distintas prioridades.

---

## Compilación y ejecución

1. Clona el repositorio de github:
   ```bash
   https://github.com/FelipeRomero19/Tarea_1_Felipe_Romero.git
   ```
2. Compila el programa:
   Abre una terminal nueva en VisualStudioCode y ejecuta el siguiente comando:
   ```bash
   gcc -o tarea1 tarea1.c tdas/list.c tdas/extra.c
   ```
3. Para ver bien las instrucciones al ejecutar el programa usa:
   ```bash
   $OutputEncoding = [Console]::OutputEncoding = [Text.UTF8Encoding]::new()
   ```
4. Ahora ejecuta:
   ```bash
   ./tarea1
   ```
5. Ahora estarás viendo el menú del programa, decide que opción usar

## ¿Cómo se usa?
---
### 1. Registrar ticket

Ingresa el número de ticket y una descripción. El programa asigna automáticamente la prioridad como "Baja"

**Ejemplo:**
```
Por favor ingrese el número de su ticket:
123456789
```
Una vez ingresado un ID válido(no repetido y que sean solo números) el programa te pedirá una descripción breve del problema
**Ejemplo:**
```
Por favor ingrese una breve descripción de su problema (máx. 200 caracteres, mín. 1 caracter):
Se cayó mi computador al agua
```
Seguido de esto el programa te pedirá apretar un botón y te mostrará los datos ingresados junto a la hora en la que se ingresó el ticket
**Ejemplo:**
```
Ticket creado como ID: 123456789
Descripción: Por favor ingrese una breve descripción de su problema (máx. 200 caracteres, mín. 1 caracter):
Se cayó mi computador al agua
Prioridad: Baja
Fecha y Hora: 23:51:12

¡Su ticket ha sido registrado con éxito!
Presione una tecla para continuar...
```
---
### 2. Cambiar prioridad

Permite cambiar la prioridad de un ticket existente. La prioridad puede estar escrita de cualquier manera, sin importar mayúsculas o minúsculas, solo importa que sea "Alta", "Media" o "Baja".

**Ejemplo:**
```
Ingrese el ticket al cual desea cambiar su prioridad
2
Ingrese la nueva prioridad:
alta
```

---

### 3. Ver tickets pendientes

Muestra los tickets en orden de prioridad y hora de llegada. Priorizando y poniendo primero en la lista las prioridades más altas y luego ordenando por hora, priorizando la hora más antigua

**Ejemplo de salida:**
```
ID: 123456789
Descripción: No prende el computador
Prioridad: Alta
Hora de ingreso: 16:42:10

ID: 3456
Descripción: No prende mi celular
Prioridad: Baja
Hora de ingreso: 17:42:10
```

---

### 4. Atender ticket

Atiende al cliente con mayor prioridad (o más antiguo si hay prioridades iguales). Luego lo elimina de la lista

**Ejemplo de salida:**
```
Inicio del procesamiento de ticket
ID del Ticket: 123456789
Descripción del problema: No prende el computador
Prioridad actual del Ticket: Alta
Hora de ingreso del Ticket: 16:42:10

El ticket ha sido procesado con éxito y ha sido eliminado de la lista
Presione una tecla para continuar...
```

---

### 5. Buscar ticket por ID

Busca un ticket y muestra su información. Si el ID ingresado no es válido mostrará un mensaje, si el ID no ha sido ingresado mostrará un mensaje y si la lista no tiene ningún ticket también lo mostrará

**Ejemplo:**
```
Por favor ingrese el ID del ticket que desea buscar
123
ID del Ticket: 123
Descripción del problema: Se cayó mi celular
Prioridad actual del Ticket: Baja
Hora de ingreso del Ticket: 21:51:12
```

---

### 6. Salir

Finaliza el programa.

**Salida:**
```
Cerrando sistema de tickets.
```

---

## Reglas

- El ID debe tener solo números (máximo 10 caracteres).
- Prioridades válidas: alta, media y baja (sin importar mayúsculas).
- Los tickets se ordenan automáticamente por prioridad y hora de ingreso.

---
