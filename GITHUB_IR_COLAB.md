# Įkėlimas ir užbaigimas

## 1. Sukurti GitHub saugyklą
1. Prisijunk prie [savo GitHub profilio](https://github.com/Laran20).
2. Spausk **+ → New repository**. Siūlomas pavadinimas: `DI-programavimo-klaidu-analize`.
3. Aprašymas: „1 namų darbas: Python klaidų analizės Colab prototipas su Gemini API“.
4. Pasirink matomumą pagal dėstytojo reikalavimus. Vieša saugykla leidžia dėstytojui peržiūrėti be pakvietimo. Spausk **Create repository**.
5. Išarchyvuok šį ZIP savo kompiuteryje. Atidaryk `DI_klaidu_analize_ND1` katalogą.
6. GitHub pasirink **uploading an existing file** arba **Add file → Upload files**. Nutempk šio katalogo TURINĮ: README, užrašyną ir visus data, prompts, diagrams katalogus. ZIP failo vietoje katalogų nekelk. Įkelk ir `.gitignore`.
7. Įrašo tekstas: `Pridėtas pirmo namų darbo prototipas`. Spausk **Commit changes**.
8. Saugyklos šaknyje turi matytis `/data/`, `/prompts/`, `/diagrams/` ir `.ipynb`.

## 2. Paleisti Colab ir įkelti tikrus atsakymus
1. Įkelk užrašyną į [Colab](https://colab.research.google.com/).
2. Į Secrets įdėk `GOOGLE_API_KEY`, suteik užrašynui prieigą ir paleisk visas celes iš eilės.
3. Patikrink, kad 7 žingsnyje yra 3/3 sėkmingi atsakymai ir nėra klaidų. Palygink išvestį su y. Peržiūrėjęs kodą, rankiniu būdu atskiroje celėje gali patikrinti data/examples.json pateiktus funkcijų testus.
4. Atsisiųsk vykdytą užrašyną tuo pačiu vardu. GitHub atnaujink ankstesnį .ipynb failą, kad matytųsi išvestys.
5. Rezultatų ZIP išarchyvuok ir įkelk jo `outputs/` katalogą į GitHub. Užrašyno 10 žingsnis jį atsisiunčia tik jei gauti visi trys atsakymai.
6. README būsenos sakinį pakeisk į „Užrašynas paleistas su Gemini API; tikri atsakymai pateikti outputs/ ir užrašyno išvestyse“. Tai daryk tik gavęs tikrus rezultatus.
7. Dėstytojui pateik konkrečios saugyklos, o ne profilio nuorodą. Užduoties paveikslėlyje 1.2.2 terminas nurodytas 10-15.

## Prieš pateikiant
- Ar yra 3 (X,y) poros ir testavimo promptas?
- Ar matomos PlantUML ir Mermaid versijos?
- Ar užrašynas rodo 3 tikrus Gemini atsakymus, kodo paaiškinimą ir grafiką?
- Ar API rakto nėra nei kode, nei išvestyse, nei saugyklos failuose?
- Ar užrašynas atsidaro GitHub ir Colab?

Jei saugykla jau sukurta kitu pavadinimu, naudok ją; šis paketas dar nėra publikuotas tavo paskyroje.
