# Topographía

[![Stato del repository: archiviato](https://img.shields.io/badge/stato-archiviato-inactive?style=for-the-badge)](https://github.com/ouitoulia/topographia?style=for-the-badge)
![GitHub](https://img.shields.io/github/license/ouitoulia/topographia?style=for-the-badge)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/ouitoulia/topographia?sort=semver&style=for-the-badge)
![Packagist Dependency Version](https://img.shields.io/packagist/dependency-v/ouitoulia/topographia/drupal/core-recommended?style=for-the-badge)
![Packagist Downloads](https://img.shields.io/packagist/dt/ouitoulia/topographia?style=for-the-badge)

> ⚠ **Questo repository è archiviato. Le funzionalità sono state spostate su `ouitoulia/themethla`**

[Topographía](https://www.grecoantico.com/dizionario-italiano-greco-antico.php?parola=topografia)
è un modulo Drupal che gestisce il tipo di contenuto Luogo definito nell'[architettura
dei contenuti delle Scuole v1.0](https://designers.italia.it/files/resources/modelli/scuole/adotta-il-modello-di-sito-scolastico/definisci-architettura-e-contenuti/Architettura-informazione-sito-scuole.ods).

## Requisiti
- Drupal: >= 10
- Profilo Drupal: `minimal`
- Moduli contrib: `address`, `conditional_field`, `field_group`, `goefield`, `leafleat`, `office_hours`, `paragraphs` `toc_js`
- Moduli Ouitoulìa: `themethla`

## Installazione
Per aggiungere il modulo alla tua installazione esegui:
```bash
$ composer require ouitoulia/topographia
$ drush -y pm:install topographia
```
Le dipendenze verranno installate automaticamente.

## Implementazione tipo Luogo
| Architettura                      | Implementazione                                           | Note                                             |
|-----------------------------------|-----------------------------------------------------------|--------------------------------------------------|
| Nome del luogo                    | title                                                     |                                                  |
| Descrizione breve                 | field_abstract                                            |                                                  |
| Argomenti                         | field_argomenti                                           | Vocabolario `argomenti` (Le parole della scuola) |
| Tipologia luogo                   | field_tipologia_luogo                                     | Vocabolario `tipologia_luoghi`                   |
| Immagine in evidenza              | field_copertina                                           | Riferimento Media `image`                        |
| Video                             | field_video                                               | Riferimento Media `video`                        |
| Galleria immagini                 | field_galleria_immagini                                   | Riferimento Media `image`                        |
| Descrizione estesa                | body                                                      |                                                  |
| Elementi di interesse nel luogo   | field_elementi_di_interesse                               | Riferimento Paragraphs `drupal/bootstrap_italia` |
| Parte di                          | field_luoghi                                              | Riferimento tipo di contenuto `Luogo`            |
| Indirizzo                         | field_indirizzo                                           | Modulo `drupal/address`                          |
| - CAP                             |                                                           | Incluso in field_indirizzo                       |
| Posizione GPS                     | field_coordinate_geografiche                              | Modulo `drupal/geofield`                         |
| Orario per il pubblico            | field_orario_pubblico                                     | Modulo `drupal/office_hours`                     |
| Email                             | field_email                                               |                                                  |
| Telefono                          | field_telefono                                            |                                                  |
| Modalità accesso                  | field_attributi_luogo                                     | Vocabolario `attributi_luogo`                    |
| Servizi presenti nel luogo        | **View relazione con CT `servizio`**                      |                                                  |
| Il luogo è sede di                | **View relazione con CT `struttura_organizzativa`**       |                                                  |
| Strutture che gestiscono il luogo | **View relazione con CT `struttura_organizzativa`**       |                                                  |
| Persone che gestiscono il luogo   | **View relazione con CT `persona`**                       |                                                  |
| Riferimento telefonico            | **View relazione con CT `struttura_organizzativa`**       |                                                  |
| Riferimento email                 | **View relazione con CT `struttura_organizzativa`**       |                                                  |
| Ulteriori informazioni            | field_extra_info                                          | Riferimento Paragraphs `drupal/bootstrap_italia` |
| Spazio prenotabile                | field_prenotabile                                         |                                                  |
| Anno di costruzione               | field_anno_costruzione                                    |                                                  |
| Numero Piani                      | field_numero_piani                                        |                                                  |
| Posti a sedere                    | field_posti                                               |                                                  |
| Metadati                          | **display**                                               |                                                  |
| Correlati: novità                 | **View relazione altri CT con `field_persone`, `author`** |                                                  |
| Codice edificio                   | field_codice_identificativo                               |                                                  |
| Codice comune                     | field_codice_catastale_comune                             |                                                  |
| Descrizione codice comune         |                                                           | **Non implementato**                             |
| Uso scolastico                    | field_uso_scolastico                                      |                                                  |
| Altri usi                         | field_destinazione_uso                                    | Vocabolario `destinazione_uso`                   |
| Anno adattamento                  | field_anno_adattamento                                    |                                                  |
| Superficie area totale            | field_superficie_area_totale                              |                                                  |
| Superficie area libera            | field_superficie_area_libera                              |                                                  |
| Volume                            | field_volume                                              |                                                  |

## License

Copyright (C) 2023 https://github.com/ouitoulia

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License version 3 as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

Questo è un software libero: puoi ridistribuirlo e/o modificarlo secondo i termini della GNU General Public License versione 3 pubblicata dalla Free Software Foundation.

Questo programma è distribuito nella speranza che possa essere utile, ma SENZA ALCUNA GARANZIA; senza nemmeno la garanzia implicita di COMMERCIABILITÀ o IDONEITÀ PER UNO SCOPO PARTICOLARE. Vedere la GNU General Public License per maggiori dettagli.