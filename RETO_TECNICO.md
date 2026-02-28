# RETO TÉCNICO: PRUEBA DE TRABAJO (PoW)

## MISIÓN: NORMALIZACIÓN DE INVENTARIO DESESTRUCTURADO

### CONTEXTO OPERATIVO
**Caso H1: HULO (Humanitarian Logistics Cooperative)**

Detectamos una fragmentación crítica de datos de inventario entre 19 ONGs globales que impide la coordinación efectiva de ayuda humanitaria. Cada organización utiliza formatos inconsistentes, nomenclaturas diferentes y estructuras de datos incompatibles.

### EL PROBLEMA

```java
// DATOS DESESTRUCTURADOS DE 19 ONGs
String[][] inventory = {
    {"ONG_A", "Medicamentos", "Aspirina", "500", "unidades"},
    {"ORG_B", "Comida", "Arroz", "1000", "kg"},
    {"NGO_C", "Agua", "Potable", "2000", "litros"},
    {"ONG_D", "Medical", "Ibuprofeno", "300", "capsulas"},
    {"ORG_E", "Food", "Pasta", "800", "paquetes"},
    {"NGO_F", "Water", "Purificada", "1500", "botellas"},
    {"ONG_G", "Medicinas", "Paracetamol", "400", "tabletas"},
    {"ORG_H", "Alimentos", "Lentejas", "600", "kg"},
    {"NGO_I", "H2O", "Potable", "1800", "garrafones"},
    {"ONG_J", "Farmacia", "Amoxicilina", "200", "capsulas"},
    {"ORG_K", "Nutrición", "Aceite", "400", "litros"},
    {"NGO_L", "Líquidos", "Agua", "2200", "litros"},
    {"ONG_M", "Drogas", "Penicilina", "150", "viales"},
    {"ORG_N", "Comestibles", "Azúcar", "500", "kg"},
    {"NGO_O", "Bebidas", "Agua Pura", "1700", "botellas"},
    {"ONG_P", "Medicina", "Antibióticos", "250", "cajas"},
    {"ORG_Q", "Viveres", "Sal", "300", "kg"},
    {"NGO_R", "Hidratación", "Agua", "1900", "litros"},
    {"ONG_S", "Fármacos", "Vitamina C", "600", "frascos"}
};
```

### PROBLEMAS IDENTIFICADOS

1. **Nomenclatura Inconsistente**: "Medicamentos" vs "Medical" vs "Medicinas" vs "Farmacia"
2. **Formatos Variables**: Unidades en "unidades", "capsulas", "tabletas", "cajas", "frascos", "viales"
3. **Categorías Ambiguas**: "Comida" vs "Food" vs "Alimentos" vs "Comestibles" vs "Viveres"
4. **Estructuras Heterogéneas**: Mismo tipo de dato con diferentes niveles de especificidad
5. **Falta de Normalización**: No hay taxonomía estándar ni sistema de clasificación unificado

### REQUERIMIENTOS TÉCNICOS

#### OBJETIVO PRINCIPAL
Crear un sistema en **Java 21** que normalice este inventario desestructurado en una taxonomía coherente y escalable.

#### ESPECIFICACIONES MÍNIMAS

1. **Clase de Normalización**
   - Implementar patrón Strategy para diferentes tipos de categorías
   - Usar enums para categorías normalizadas
   - Aplicar principios de Domain-Driven Design

2. **Taxonomía Estándar**
   ```java
   public enum CategoriaNormalizada {
       MEDICAMENTOS,
       ALIMENTOS, 
       AGUA,
       SUPLEMENTOS
   }
   
   public enum UnidadNormalizada {
       UNIDADES,
       CAPSULAS,
       TABLETAS,
       KG,
       LITROS,
       BOTELLAS,
       FRASCOS,
       VIALES,
       CAJAS
   }
   ```

3. **Procesamiento Inteligente**
   - Algoritmo de similitud de strings (Levenshtein o similar)
   - Mapeo automático de términos variantes a categorías normalizadas
   - Manejo de excepciones y logging estructurado

4. **Salida Estructurada**
   - JSON o XML normalizado
   - Estadísticas de consolidación
   - Reporte de transformaciones aplicadas

#### CRITERIOS DE EVALUACIÓN

- **Rigor Técnico**: Arquitectura limpia, patrones de diseño apropiados
- **Escalabilidad**: Sistema que pueda manejar más ONGs y categorías
- **Mantenibilidad**: Código documentado, testable y extensible
- **Performance**: Procesamiento eficiente de grandes volúmenes de datos
- **Robustez**: Manejo elegante de casos edge y datos corruptos

### ENTREGABLES ESPERADOS

1. **Código Fuente** en Java 21
2. **Test Unitarios** con casos de borde
3. **README** con arquitectura y decisiones de diseño
4. **Demo Funcional** que muestre la transformación

### IMPACTO DE LA SOLUCIÓN

Una implementación exitosa permitirá:
- Coordinación efectiva entre 19 ONGs
- Reducción de duplicidad de recursos
- Optimización de distribución de ayuda
- Base para sistema escalable a nivel global

---

**ESTE RETO ES TU PUERTA DE INGRESO A LA BRIGADA DEL ÁGUILA**

Demuestra tu capacidad de transformar el caos en coherencia. La ayuda humanitaria no puede esperar por burocracia.

*Brigada del Águila - Restauración de Coherencia Sistémica*
