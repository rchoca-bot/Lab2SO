# 📘 Documentación del Proyecto: Simulador de Planificación de Procesos

## Introducción
La planificación de procesos es una de las funciones más importantes de los sistemas operativos, ya que determina qué proceso se ejecutará en la CPU en un momento dado.  
Este proyecto implementa un **simulador interactivo** que permite experimentar con distintos algoritmos de planificación, visualizar sus resultados y comparar métricas clave.

---

## Objetivos
- Simular de manera gráfica la ejecución de procesos con diferentes algoritmos de planificación.
- Permitir la creación de procesos con parámetros personalizables.
- Visualizar el comportamiento de los procesos en un **diagrama de Gantt**.
- Calcular y mostrar métricas fundamentales de rendimiento (Waiting Time, Turnaround Time, Response Time).
- Proporcionar una herramienta educativa para comprender cómo se comportan los algoritmos en distintos escenarios.

---

## Algoritmos implementados

### 🔹 FCFS (First Come, First Served)
- **Tipo:** No expropiativo.  
- **Funcionamiento:** Los procesos se atienden en el orden en que llegan a la cola de listos.  
- **Ventaja:** Fácil de implementar.  
- **Desventaja:** Puede producir el problema de convoy (procesos cortos esperan a uno largo).

---

### 🔹 SJF (Shortest Job First)
- **Tipo:** No expropiativo.  
- **Funcionamiento:** Se selecciona el proceso con menor ráfaga (burst) disponible.  
- **Ventaja:** Minimiza el tiempo promedio de espera.  
- **Desventaja:** Posible inanición de procesos largos.

---

### 🔹 SRTF (Shortest Remaining Time First)
- **Tipo:** Expropiativo.  
- **Funcionamiento:** Siempre se ejecuta el proceso con menor tiempo restante de CPU.  
- **Ventaja:** Reduce tiempos de espera para procesos cortos.  
- **Desventaja:** Mayor sobrecarga y posibles cambios frecuentes de contexto.

---

### 🔹 Round Robin (RR)
- **Tipo:** Expropiativo.  
- **Funcionamiento:** Cada proceso recibe un quantum (tiempo fijo). Si no termina, se interrumpe y regresa a la cola.  
- **Ventaja:** Justo y equitativo, ideal para sistemas interactivos.  
- **Desventaja:** El rendimiento depende del tamaño del quantum.

---

## Métricas utilizadas

El simulador calcula automáticamente:

- **Start:** tiempo en que el proceso comienza a ejecutarse.  
- **Finish:** tiempo en que el proceso finaliza.  
- **WT (Waiting Time):** tiempo de espera en cola antes de ejecutarse.  
  - Fórmula: `WT = TAT - Burst`
- **TAT (Turnaround Time):** tiempo total desde la llegada hasta la finalización.  
  - Fórmula: `TAT = Finish - Arrival`
- **RT (Response Time):** tiempo desde la llegada hasta la primera ejecución.  
  - Fórmula: `RT = Start - Arrival`

Además, se muestran los promedios de estas métricas para evaluar el rendimiento general del algoritmo.

---

## Funcionamiento del simulador

1. **Crear procesos** ingresando:
   - Nombre
   - Tiempo en CPU (burst)
   - Instante de llegada
   - Quantum (opcional)

2. **Seleccionar algoritmo y parámetros**:
   - Algoritmo de planificación
   - Quantum global (usado en RR o si el proceso no define uno)
   - Duración de 1 unidad de tiempo en segundos

3. **Ejecutar simulación** para visualizar:
   - **Diagrama de Gantt**
   - **Historial de ejecución**
   - **Colas de listos por tiempo**
   - **Métricas individuales y promedios**

---

## Conclusión
Este simulador permite observar de forma clara cómo los diferentes algoritmos de planificación afectan el rendimiento de un conjunto de procesos.  
Es una herramienta útil para **estudiantes y docentes** de sistemas operativos, ya que convierte conceptos teóricos en resultados visuales y prácticos.# Lab2SO
