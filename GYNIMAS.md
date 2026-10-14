# Trumpas paaiškinimas gynimui

Mano tema – DI pagrįsta programavimo klaidų analizės sistema. Pirmą prototipą sukūriau Python kalbos kodui analizuoti Google Colab aplinkoje. Jis skirtas pradedančiam programuotojui, kuris mato klaidą, bet ne visada supranta jos priežastį.

Vartotojas pateikia kodą, paskirties aprašymą ir klaidos pranešimą. Programa patikrina įvestį ir sudaro užklausą Gemini API. Modelis sugeneruoja klaidos tipą, paaiškinimą, pataisytą kodą, testavimo pavyzdžius ir prevencijos patarimą. Pydantic patikrina atsakymo struktūrą, o ast.parse – pataisyto kodo sintaksę. Rezultatas parodomas ir išsaugomas JSON formatu.

Duomenų kataloge yra trys X ir y poros. X reiškia įvestį, y – mano parengtą laukiamą rezultatą. Modelio atsakymą žymiu ŷ. Tik X siunčiu modeliui; y naudoju palyginimui. Pavyzdžiai apima trūkstamą dvitaškį, dalybą iš nulio ir neteisingą nuolaidos formulę.

Generatyvinis DI šiame darbe pats sukuria paaiškinimą ir taisymo pasiūlymą. Tai nėra trijų iš anksto paruoštų atsakymų parinkimas. Modelis papildomai nemokomas. Mano Python kodas paruošia duomenis, iškviečia API ir patikrina rezultatų formatą.

Pirmiausia sistemą projektavau PlantUML, o paskui tas pačias diagramas pateikiau Mermaid. Projektavimo ir testavimo promptai išsaugoti prompts kataloge.

Pagrindinis apribojimas – tinkama sintaksė dar nereiškia teisingos programos logikos. Todėl yra etalonai ir konkretūs testavimo atvejai; modelio kodas automatiškai nevykdomas. Trys pavyzdžiai parodo veikimo eigą, tačiau neįrodo tikslumo visoms klaidoms.

## Dažniausi klausimai
| Klausimas | Trumpas atsakymas |
|---|---|
| Kas yra API? | Sąsaja, per kurią mano programa siunčia užklausą Gemini ir gauna atsakymą. |
| Kas yra promptas? | Instrukcija modeliui, ką analizuoti ir kokį rezultatą pateikti. |
| Kodėl JSON? | Kad atsakymą būtų galima patikimai nuskaityti, tikrinti ir išsaugoti. |
| Kam skirtas Pydantic? | Atsakymo laukams, tipams ir minimaliems reikalavimams tikrinti. |
| Ką daro ast.parse? | Patikrina Python sintaksę, bet nevykdo kodo ir netikrina visos logikos. |
| Ar sistema yra autonominis agentas? | Tai vieno analizės žingsnio DI asistentas; savarankiško įrankių vykdymo ciklo ši versija neturi. |
| Ar raktas yra GitHub? | Ne, jis laikomas Colab Secrets arba įvedamas paslėptai. |
| Kaip įrodyti, kad veikia? | Paleisti visas celes, parodyti 3 tikrus atsakymus, suvestinę ir rezultatų JSON. |

Pristatydamas rezultatus remkis tik tuo, kas matoma po tikro Colab paleidimo.
