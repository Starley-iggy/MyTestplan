# Technisch Testplan

## Algemeen

| Onderdeel        | Omschrijving                               |
| ---------------- | ------------------------------------------ |
| Integratie       | CityPermit ↔ Integratieframework ↔ Key2DDS |
| Datum uitvoering | 21-09-2005                                 |
| Uitvoerder       | Team Integratie                            |

---

# Doelstelling

Het doel van dit technisch testplan is het valideren van de technische werking van de integratieketen inclusief beveiliging, netwerkverbindingen, authenticatie, monitoring en foutafhandeling.

---

# Scope

## In Scope

* MTLS authenticatie
* Routering
* Berichtvalidatie
* Logging
* Monitoring
* Retry mechanisme
* Performance
* HTTP-statuscodes

## Out of Scope

* Inhoudelijke beoordeling van gegevens
* Gebruikersacceptatie

---

# Technische Testscenario's

## TT-01 MTLS Authenticatie

### Verwacht resultaat

* Alleen geautoriseerde certificaten krijgen toegang.

### Verwachte status

* 200 OK
* 401 Unauthorized
* 403 Forbidden

Resultaat: PASS / FAIL

---

## TT-02 XML/STUF-ZKN Validatie

### Verwacht resultaat

* Ongeldige XML wordt afgewezen.

### Verwachte status

* 400 Bad Request

Resultaat: PASS / FAIL

---

## TT-03 Endpoint beschikbaarheid

### Verwacht resultaat

* Endpoint is bereikbaar.

### Verwachte status

* 200 OK

Resultaat: PASS / FAIL

---

## TT-04 Key2DDS niet beschikbaar

### Verwacht resultaat

* Fout wordt geregistreerd.

### Verwachte status

* 503 Service Unavailable

Resultaat: PASS / FAIL

---

## TT-05 Timeout Scenario

### Verwacht resultaat

* Timeout wordt correct afgehandeld.

### Verwachte status

* 504 Gateway Timeout

Resultaat: PASS / FAIL

---

## TT-06 Retry Mechanisme

### Verwacht resultaat

* Bericht wordt opnieuw aangeboden.

### Verwachte status

* Eerste poging: 503
* Tweede poging: 200

Resultaat: PASS / FAIL

---

## TT-07 Logging Controle

### Verwacht resultaat

* Request zichtbaar.
* Response zichtbaar.
* Correlatie-ID aanwezig.

Resultaat: PASS / FAIL

---

## TT-08 Monitoring Controle

### Verwacht resultaat

* Monitoring events zichtbaar.
* Dashboards bijgewerkt.

Resultaat: PASS / FAIL

---

## TT-09 Performance Test

### Verwacht resultaat

* Verwerking < 5 seconden.
* Geen fouten bij piekbelasting.

Resultaat: PASS / FAIL

---

# HTTP Statuscode Matrix

| Statuscode | Omschrijving          |
| ---------- | --------------------- |
| 200        | OK                    |
| 400        | Bad Request           |
| 401        | Unauthorized          |
| 403        | Forbidden             |
| 404        | Not Found             |
| 409        | Conflict              |
| 422        | Unprocessable Entity  |
| 500        | Internal Server Error |
| 502        | Bad Gateway           |
| 503        | Service Unavailable   |
| 504        | Gateway Timeout       |

---

# Goedkeuring

| Rol              | Naam | Akkoord |
| ---------------- | ---- | ------- |
| Integratie Team  |      |         |
| Applicatiebeheer |      |         |
| Technisch Beheer |      |         |
