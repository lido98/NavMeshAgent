# NavMeshAgent

**Integrantes:**
* Raúl Beltrán Gómez (C-312) (@rb58853)
* Lidier Robaina Caraballo (C-312) (@lido98)

**Objetivo:** Decidir y simular los movimientos óptimos de agentes de navegación que interactúan entre ellos donde influyen condiciones climatológicas, estacionales y del terreno.

## Descripción
* **Terreno**: Se define como un grafo de aristas con costo donde los vértices son posiciones accesibles a las cuales se pueden mover los agentes (cada agente puede tener posiciones accesibles distintas a otros) y las aristas definen si se puede ir de un vértice a otro. Cada movimiento (arista) tiene un costo de tiempo en el cual la recorre, esto está dado por las condiciones del terreno como puede ser hierva alta, fango, agua y otros. Un terreno está definido en el espacio y no en el plano, ir de un vértice a otro puede ser más costoso por estar en subida en una elevación y viceversa al estar en bajada (o por la dirección del viento, y otros), por lo que el grafo de movimiento tiene valores para cada dirección de la arista (realmente es un grafo formado por arcos, donde dos arcos entre los mismos vértices pueden o no tener el mismo costo de recorrido).
* **Estaciones:** Cada estación traerá consigo las condiciones climatológicas de la misma y los cambios en el terreno a los que esto conlleva. El otoño trae consigo vientos más fuertes y caída de las hojas que obstaculizan el terreno, el invierno convierte el agua en hielo (por ejemplo un río congelado pasa a ser transitable) y se produce acumulación de nieve, en primavera la hierba crece más y algunos recorridos serán más costosos, en verano la lluvia creará charcos, los pantanos serán más difíciles de transitar, entre otras condiciones que se pueden dar.
* **Condiciones climatológicas:** Las condiciones del clima o eventos arbitrarios que pueden suceder en un escenario provocan cambios en las condiciones del terreno, por ejemplo, la caída de un árbol, las lluvias intensas, las tormentas de nieve, los vientos fuertes, el desborde de un río, entre otros.
* **Agentes de navegación:** Los agentes son los encargados de interactuar con el medio y moverse de la forma "más inteligente" posible de una posición a otra, los agentes interactúan entre ellos y, dependendiendo de ciertas condiciones específicas de cada agente, hay lugares que pueden ser alcanzables por algunos agentes y otros no, por ejemplo: agentes con habilidad para volar podrán alcanzar algunas elevaciones que otros agentes no pueden, agentes más grandes pueden saltar obstáculos que otros no pueden, agentes más pesados son menos afectados por el viento que otros con menos peso. Un agente no puede ir a la posición de otro agente, es decir, dos agentes no pueden coincidir en el mismo vértice del grafo.

