# Duomenys: (X, y) poros
X – Python kodas, pageidaujamas elgesys ir klaidos pranešimas. y – autoriaus parengtas etaloninis sprendimas, su kuriuo lyginama modelio išvestis ŷ.
Tai trys mokomieji, specialiai sukurti pavyzdžiai, o ne mokymo duomenų rinkinys ar realūs Gemini atsakymai. Modelis papildomai neapmokomas.

| ID | Klaida | Tikėtinas taisymas |
|---|---|---|
| 01 | Sintaksės | Dvitaškis po def |
| 02 | Vykdymo | Tuščio sąrašo patikra |
| 03 | Loginė | Nuolaidos atėmimas iš kainos |

Kiekviename kataloge yra X_input.json, y_expected.json, buggy.py ir reference_fixed.py. examples.json sujungia poras ir nepriklausomus checks testų duomenis. Į Gemini siunčiamas tik X. y ir checks naudojami tik po atsakymo gavimo vertinimui. Kitas teisingas kodas gali skirtis nuo etalono tekstu.
