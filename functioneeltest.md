# Functioneel Testplan

## Algemeen

| Onderdeel        | Omschrijving                                           |
| ---------------- | ------------------------------------------------------ |
| Integratie       | CityPermit naar Key2DDS                                |
| Eigenaar         | Starley Igbinomwhaia Briggs                            |
| Gemeente         | Leeuwarden                                             |
| Eindgebruikers   | John Doe                                               |
| Doel             | Valideren van de functionele werking van de integratie |
| Datum uitvoering | 21-09-2005                                             |
| Uitvoerder       | Team Integratie                                        |

---

# Doelstelling

Het doel van dit functioneel testplan is vaststellen dat de bedrijfsprocessen die door de integratie worden ondersteund correct functioneren en dat gegevens correct worden uitgewisseld tussen CityPermit en Key2DDS.

---

# Scope

## In Scope

* Aanmaken van zaken.
* Muteren van zaken.
* Overdracht van zaakgegevens.
* Validatie van bedrijfsregels.
* Verwerking van foutieve invoer.

## Out of Scope

* Technische infrastructuur.
* Netwerkverbindingen.
* Certificaten.
* Performance testen.

---

# Testdata

| Testdata      | Doel               |
| ------------- | ------------------ |
| TEST-ZAAK-001 | Nieuwe zaak        |
| TEST-ZAAK-002 | Wijziging zaak     |
| TEST-ZAAK-003 | Dubbele zaak       |
| TEST-ZAAK-004 | Onvolledig bericht |

---

# Functionele Testscenario's

## FT-01 Nieuwe zaak aanmaken

### Verwacht resultaat

* Zaak wordt aangemaakt in Key2DDS.
* Alle gegevens zijn correct overgenomen.

Resultaat: PASS / FAIL

---

## FT-02 Wijzigen bestaande zaak

### Verwacht resultaat

* Wijzigingen worden correct verwerkt.
* Zaak wordt bijgewerkt.

Resultaat: PASS / FAIL

---

## FT-03 Dubbele zaak aanbieden

### Verwacht resultaat

* Dubbele verwerking wordt voorkomen.

Resultaat: PASS / FAIL

---

## FT-04 Verplicht veld ontbreekt

### Verwacht resultaat

* Bericht wordt afgewezen.
* Foutmelding wordt geregistreerd.

Resultaat: PASS / FAIL

---

## FT-05 Controle gegevensintegriteit

### Verwacht resultaat

* Verzonden gegevens komen volledig en ongewijzigd aan.

Resultaat: PASS / FAIL

---

# Acceptatiecriteria

* Alle functionele testcases zijn succesvol uitgevoerd.
* Geen kritische bevindingen openstaand.
* Functioneel beheer geeft akkoord.

---

# Goedkeuring

| Rol                | Naam | Akkoord |
| ------------------ | ---- | ------- |
| Functioneel Beheer |      |         |
| Product Owner      |      |         |
