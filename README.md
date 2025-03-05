
# Control de Movimiento - CLASE 2

# Control en Cascada

El control en cascada es una estrategia de control utilizada para mejorar la estabilidad y respuesta de un sistema mediante la implementación de dos o más lazos de control jerárquicos.

### Esquema
![Figura de prueba](IMAGES/CASCADA.png)

###  Componentes del Control en Cascada
- **Controlador Primario (C1)**: Responsable de la variable principal.
- **Controlador Secundario (C2)**: Regula una variable interna más rápida.
- **Procesos G1 y G2**: Modelos matemáticos de los procesos controlados.

### Selección de Controladores
- C2 debe ser más rápido que C1.
- C2 suele ser **P o PI** para evitar ralentización.
- C1 puede ser **PI o PID** para minimizar el error.

### Casos de Aplicación
- Cuando las perturbaciones afectan el tiempo de establecimiento.
- Cuando hay variables internas más rápidas disponibles.
- Cuando se desea mejorar la dinámica de la variable controlada.

## Métodos de Sintonización
#### Metodologías empíricas
- **Lazo abierto**: Se ajustan los controladores de forma independiente, por metodos conocidos y la interacción entre lazos.
  
  Ejemplo
  ![Figura de prueba](images/CALDERO.png).
  
- **Lazo cerrado**: Se utiliza la realimentación para mejorar la respuesta.

#### 5.2. Métodos específicos
- **Método Austin (1986)**: Ajusta ambos lazos con una sola prueba.
- **Método Hang (1994)**: Basado en pruebas de relé.

### 6. Ejemplos Adicionales
1. **Sistema de climatización**: El controlador primario ajusta la temperatura, mientras que el secundario regula el flujo de aire.
2. **Control de nivel en un tanque**: Un controlador ajusta el flujo de entrada mientras que otro regula la presión de salida.

### 7. Ecuaciones
- Función de transferencia del proceso secundario:
  \[ G_2 = \frac{0.5e^{-s}}{2s+1} \]
- Función de transferencia del proceso primario:
  \[ G_1 = \frac{e^{-10s}}{15s+1} \]
- Cálculo de ganancia del controlador secundario:
  \[ K_{c2} = \frac{0.9}{K_2} \frac{τ_2}{t_m} \]

### 8. Figuras
1. **Diagrama de bloques de un control en cascada**.
2. **Respuesta temporal de un sistema en cascada comparado con un sistema de control simple**.

### 9. Tablas
| Controlador | Tipo Recomendado |
|------------|-----------------|
| C1 (Primario) | PI o PID |
| C2 (Secundario) | P o PI |

### 10. Ejercicios
1. Diseña un sistema de control en cascada para una planta de calentamiento de líquidos.
2. Calcula la ganancia de los controladores para un sistema con parámetros específicos.

### 11. Conclusiones
- El control en cascada mejora la estabilidad y reduce los efectos de perturbaciones.
- La selección adecuada de controladores es clave para optimizar el desempeño.
- Diferentes métodos de sintonización pueden utilizarse dependiendo de la aplicación.

### 12. Referencias
- Smith, C., & Corripio, A. *Principles and Practice of Automatic Process Control*.
- Hang, C.C. *Relay Feedback Auto-Tuning Cascade Controllers*. IEEE, 1994.
- Austin, J. *Cascade Control Tuning Methods*. Industrial Engineering, 1986.

