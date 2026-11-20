# Previsualización M3U Elcano adaptada

**Solo vista previa.** Esta rama no modifica `main`, no cambia el M3U que consume la web y no provoca despliegues.

## Resultado de la simulación

- TXT de Elcano: **162 enlaces**, 162 hashes únicos.
- M3U adaptado: **163 enlaces** (162 de Elcano + 1 enlace antiguo conservado).
- Tarjetas simuladas con la misma clave que usa la web (categoría + nombre base): **69**.
- Categorías: **21**.
- Hashes duplicados: **0**.
- Canal `luz`: **eliminado**, incluidos sus dos enlaces.
- Hashes con formato incorrecto: **0**.

## Qué se ha conservado

- Cabecera EPG y opciones VLC originales.
- Categorías, nombres visibles, emojis, logotipos y `tvg-id` de los canales ya existentes.
- Agrupación de calidades y enlaces en una tarjeta por canal.
- El canal antiguo **DAZN LaLiga 2**, que no aparece en el TXT nuevo, se conserva con su enlace anterior en vez de borrarlo sin autorización.

## Alias reconocidos

- MOVISTAR PLUS → MOVISTAR PLUS+
- SPORT TV3 → SPORT TV 3
- UFC → PARAMOUNT+ UFC

## Clasificación nueva

- RALLY TV → MOTOR | RALLYS (nueva categoría).
- A Punt → TELEVISIÓN | AUTONÓMICAS.
- DAZN 3 → DEPORTES | DAZN.
- M+ Baloncesto 4 → DEPORTES | BALONCESTO.
- M+ Liga de Campeones 9 → FÚTBOL | LIGA DE CAMPEONES.
- Sky Sport MotoGP → MOTOR | MOTOGP.
- `luz` se ha dejado provisionalmente en DEPORTES | INTERNACIONAL: confirmar su categoría antes de publicar.

## Canales resultantes por categoría

- **FÚTBOL | LALIGA:** DAZN LaLiga; M+ LaLiga; M+ LaLiga 2; M+ LaLiga 3; DAZN LaLiga 2 (antiguo conservado)
- **FÚTBOL | HYPERMOTION:** LaLiga TV Hypermotion; LaLiga TV Hypermotion 2; LaLiga TV Hypermotion 3
- **FÚTBOL | LIGA DE CAMPEONES:** M+ Liga de Campeones; M+ Liga de Campeones 2; M+ Liga de Campeones 3; M+ Liga de Campeones 4; M+ Liga de Campeones 5; M+ Liga de Campeones 6; M+ Liga de Campeones 7; M+ Liga de Campeones 8; M+ Liga de Campeones 9
- **FÚTBOL | RFEF:** RFEF TV
- **FÚTBOL | CLUBES:** Real Madrid TV
- **DEPORTES | BALONCESTO:** DAZN Baloncesto; DAZN Baloncesto 2; DAZN Baloncesto 3; M+ Baloncesto; M+ Baloncesto 2; M+ Baloncesto 3; M+ Baloncesto 4; NBA ESPN; NBA League Pass
- **DEPORTES | DAZN:** DAZN 1; DAZN 2; DAZN 3; DAZN 4
- **DEPORTES | MOVISTAR:** M+ Deportes (2–8); M+ Vamos (2–3)
- **DEPORTES | EUROSPORT:** Eurosport 1; Eurosport 2
- **DEPORTES | GOLF:** M+ Golf; M+ Golf 2
- **DEPORTES | TENIS:** Sky Sport Tennis; Tennis Channel
- **MOTOR | FÓRMULA 1:** DAZN F1
- **MOTOR | MOTOGP:** DAZN MotoGP; Sky Sport MotoGP
- **MOTOR | RALLYS:** RALLY TV
- **TELEVISIÓN | TDT:** Cuatro; La 1 TVE; La 2 TVE; Telecinco
- **TELEVISIÓN | AUTONÓMICAS:** A Punt; Esport3
- **MOVISTAR | GENERAL:** Movistar Plus+; M+ 0
- **DEPORTES | TELEDEPORTE:** Teledeporte
- **DEPORTES | TOROS:** Onetoro TV
- **DEPORTES | UFC:** Paramount+ UFC
- **DEPORTES | INTERNACIONAL:** beIN Sports 3 TR; beIN Sports TR; SPORT TV 3; Sport TV+

## Pendiente antes de publicar

1. Confirmar la categoría de `luz`.
2. Decidir si se conserva o se elimina DAZN LaLiga 2, ausente en el TXT nuevo.
3. Comprobar en la web de prueba que el renderizador agrupa las 69 tarjetas como se espera.
4. Revisar la correspondencia EPG de los canales nuevos: se han preservado los `tvg-id` antiguos y se han dejado los del TXT en las altas nuevas.

Nada de esto se ha publicado en `main`.
