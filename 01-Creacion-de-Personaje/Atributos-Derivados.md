# Atributos Derivados

> [!warning]
> Tablas verificadas contra el OCR limpio del Básico 2ª (PG por localización y MMR por longitud de arma corregidos).

Atributos calculados a partir de [[Caracteristicas]]. Anotarlos en la hoja en los espacios indicados.

## Puntos de magia (PM)

- PM = PER actual.
- Se gastan al lanzar conjuros; gastar PM no reduce la PER.
- Recuperación: 1/24 de la PER actual por hora (recarga completa en 24 h).
- Marcar con círculo el valor en la tabla de PM de la hoja.

## Puntos de fatiga (PF)

- PF básicos = FUE + CON.
- Marcar el total en la tabla de PF de la hoja. Ver [[Fatiga-Carga-y-Movimiento]] para uso en asaltos.

## Puntos de golpe (PG)

- PG totales = (CON + TAM) / 2, redondeando hacia arriba.
- Si PG totales llegan a 2 o menos: inconsciente. Si llegan a 0 o menos: muerte al final del asalto (ver [[Daño-y-Curacion]]).
- Reparto por localización (humanoides):

| PG tot | Pierna c/u | Abdomen | Pecho | Brazo c/u | Cabeza |
|---|---|---|---|---|---|
| 01-03 | 1 | 1 | 2 | 1 | 1 |
| 04-06 | 2 | 2 | 3 | 2 | 2 |
| 07-09 | 3 | 3 | 4 | 3 | 3 |

| 10-12 | 4 | 4 | 5 | 3 | 4 |
| 13-15 | 5 | 5 | 6 | 4 | 5 |
| 16-18 | 6 | 6 | 8 | 5 | 6 |
| 19-21 | 7 | 7 | 9 | 6 | 7 |

Fracciones hacia arriba. La suma por localizaciones supera el total: es correcto; la muerte llega por acumulación o por inutilizar zonas (ver [[Daño-y-Curacion]]).

## Modificador al daño

Sumar FUE + TAM y consultar:

| FUE+TAM | Modificador |
|---|---|
| 01-12 | -1D4 |
| 13-24 | +0 |
| 25-32 | +1D4 |
| 33-40 | +1D6 |
| 41-56 | +2D6 |
| 57+ | +1D6 más por cada 16 puntos o fracción |

- Se suma al daño del arma en ataque con éxito; la mitad (redondeando hacia arriba, p. ej. 1D4 -> 1D2) con armas arrojadizas.
- Tirar daño del arma y modificador por separado y sumar.
- Es fijo salvo que cambien FUE o TAM. Anotarlo tras cada arma.

## Momentos de reacción (MR)

El asalto tiene 10 MR (1-10). Cuanto más bajo, antes se actúa.

| Origen | Tabla |
|---|---|
| MR por DES | 01-09: 4; 10-15: 3; 16-19: 2; 20+: 1 |
| MMR por TAM (solo cuerpo a cuerpo) | 01-09: 3; 10-15: 2; 16-19: 1; 20+: 0 |

- Arrojadizas y proyectiles: MR = MR-DES (TAM cuenta 0).
- Cuerpo a cuerpo: MR = MR-DES + MMR-TAM + MMR del arma (longitud: 0-0,3 m puño/cuchillo 3; 0,4-1,1 m arma 1M 2; 1,2-2,1 m arma 2M 1; 2,2 m+ pica 0; ver [[Combate]]).
- Conjuros: MR = MR-DES + PM usados (espiritual/hechicería). Divina con potencia elegible suma igual.
- Movimiento: se empieza a mover en el MR-DES, 3 m por MR (6 m corriendo, con doble fatiga).

## Modificadores por categoría de habilidad

Cada categoría suma influencias de características:

| Categoría | Primaria (+1/-1 por punto sobre/bajo 10) | Secundaria (+1/-1 por 2 puntos) | Negativa (inversa de primaria) |
|---|---|---|---|
| Agilidad | DES | FUE | TAM |
| Comunicación | INT | PER, APA | — |
| Conocimiento | INT | — | — |
| Magia | INT, PER | DES | — |
| Manipulación | INT, DES | FUE | — |
| Percepción | INT | PER, CON | — |
| Sigilo | DES | — | TAM, PER |

- Puntos sobre 30 de característica no cuentan.
- El modificador se suma a toda habilidad de la categoría con base >0%. Si la base es 0% y luego sube a 1%+, entonces se le aplica.
- Habilidad nunca baja de 0% por modificador.
- Modificador de ataque = modificador de Manipulación. Modificador de parada = modificador de Agilidad.

#runequest/reglas

*Fuente: RuneQuest Básico 2ª Edición (Joc Internacional), Libro de Reglas, cap. Cómo Crear un Aventurero.*
