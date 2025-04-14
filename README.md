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

5. Ahora ejecuta:
   ```bash
   ./tarea1
   ```
6. Ahora estarás viendo el menú del programa, decide que opción usar

---

## ¿Cómo se usa?

### 1. Registrar ticket

Pide número de ticket y una descripción. Se crea con prioridad baja.

**Ejemplo:**
```
Ingrese número de ticket: 123456789
Descripción del problema: No prende el computador
```

---

### 2. Cambiar prioridad

Permite cambiar la prioridad de un ticket existente.

**Ejemplo:**
```
Ingrese el ticket: 123456789
Ingrese la nueva prioridad: alta
```

---

### 3. Ver tickets pendientes

Muestra los tickets en orden de prioridad y hora de llegada.

**Ejemplo de salida:**
```
ID: 123456789
Descripción: No prende el computador
Prioridad: Alta
Hora de ingreso: 16:42:10
```

---

### 4. Atender ticket

Atiende al cliente con mayor prioridad (o más antiguo si hay empate).

**Ejemplo de salida:**
```
Atendiendo ticket:
ID: 123456789
Descripción: No prende el computador
Prioridad: Alta
```

---

### 5. Buscar ticket por ID

Busca un ticket y muestra su información.

**Ejemplo:**
```
Ingrese ID del ticket: 1234567
Ticket encontrado:
ID: 123456789
Descripción: No prende el computador
Prioridad: Alta
Hora: 16:42:10
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
