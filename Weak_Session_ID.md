# Weak Session IDs - DVWA

## Nivel de seguridad: Low

En el nivel de seguridad **Low**, la generación de las cookies de sesión es extremadamente predecible.

- El valor de la cookie de sesión comienza en **0**.
- Cada vez que se regenera la sesión, simplemente se **incrementa en 1**.

Esto implica que un atacante que intercepte o adivine un ID de sesión puede predecir fácilmente los siguientes o anteriores IDs, comprometiendo otras sesiones activas en el sistema.

> **Ejemplo:**
> - Primera sesión: `PHPSESSID=0`
> - Segunda sesión: `PHPSESSID=1`
> - Tercera sesión: `PHPSESSID=2`

Este patrón hace que la **fuerza bruta de sesiones** sea trivial.

---

## Nivel de seguridad: Medium

En el nivel **Medium**, el mecanismo de generación de sesiones mejora ligeramente.

- El valor de la cookie de sesión se genera usando la función **`time()`** de PHP.
- Esto significa que la cookie está basada en la **marca temporal actual** (timestamp).

Aunque esto introduce algo de aleatoriedad temporal, **sigue siendo vulnerable** porque:

- El tiempo de creación de una sesión puede ser **estimado** con mucha precisión.
- Permite a un atacante generar sesiones potencialmente válidas basándose en una pequeña ventana de tiempo.

> **Problema:**
> El uso exclusivo de `time()` para IDs de sesión no proporciona suficiente entropía (aleatoriedad) para proteger contra ataques de predicción.

---

# Resumen

Tanto en **Low** como en **Medium**, los IDs de sesión son vulnerables a predicción y ataque.

- En **Low**, la predictibilidad es directa y trivial.
- En **Medium**, es necesaria una estimación de tiempo pero sigue siendo inseguro.

Una buena generación de sesiones debería usar funciones criptográficamente seguras, como `random_bytes()` o `openssl_random_pseudo_bytes()`.

> **Importante:** Un ID de sesión seguro debe ser impredecible, suficientemente largo y aleatorio para prevenir ataques de secuestro de sesión.
