# ND1 tęsinys: 1.3–1.5

Liutauras Turauskis · DIPf-24

Penki pagal pateiktus dėstytojo pavyzdžius pritaikyti Google Colab užrašynai.
Tai papildomos mašininio mokymosi užduotys; ankstesnis DI programavimo klaidų analizės darbas nekeičiamas.

| Užduotis | Failas | Pritaikymas |
|---|---|---|
| 1.3, TensorFlow NN | `1_3_1_Banko_duomenys_NN.ipynb` | UCI Bank Marketing; kategorijų ir skaitinių požymių apdorojimas; NN |
| 1.3, TF Decision Forests | `1_3_2_Banko_duomenys_Decision_Forests.ipynb` | Tas pats banko rinkinys; miškas, OOB, medis ir svarba |
| 1.4, CNN | `1_4_CNN_Geliu_klasifikavimas.ipynb` | Flowers Photos; CNN, MLP, filtrai ir rankinė koreliacija |
| 1.5, Transfer learning 1 | `1_5_1_Transfer_learning_Vienas_vaizdas.ipynb` | Gėlės nuotrauka; klasifikavimas, iškarpa, aptikimas ir segmentavimas |
| 1.5, Transfer learning 2 | `1_5_2_Transfer_learning_Geliu_mokymas.ipynb` | Gėlių klasės; užšaldyta bazė, nauja galva ir fine-tuning |

## Kaip paleisti

1. Atidarykite norimą `.ipynb` Google Colab (File → Upload notebook, arba GitHub).
2. Vaizdų mokymui pasirinkite Runtime → Change runtime type → T4 GPU, jei prieinama.
3. Naujoje sesijoje vykdykite Runtime → Run all. Nekeiskite ląstelių tvarkos.
4. Išsaugokite paleistą kopiją su grafikais ir rodikliais. Norėdami išsaugoti mokymo modelius,
   atsisiųskite sesijoje sukurtą `rezultatai` katalogą iki sesijos pabaigos.

Kiekvienas užrašynas savarankiškas. NN ir TFDF palyginimo lentelė automatiškai pasirodo,
jei abu paleisti toje pačioje sesijoje ir išliko `rezultatai/nn_rodikliai.json`.
TFDF naudoja izoliuotą Python 3.12 / TensorFlow 2.19 aplinką Colab Linux sistemoje.
1.5.1 HRNet modelis didesnis, todėl jo atsisiuntimui reikia laiko ir laisvos atminties.

## Duomenys ir sąžiningas vertinimas

Pasirinkti vieši, skirtingi nuo dėstytojo pavyzdžių duomenys. Banko rinkinys:
[UCI Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing),
taip pat [Kaggle verslo rinkinys](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset).
Gėlės: [TensorFlow Flowers Photos](https://www.tensorflow.org/tutorials/load_data/images).
Banko duomenims taikoma CC BY 4.0; nuotraukų autorystė pateikta atsisiunčiamo archyvo LICENSE.txt.
Banko duomenų autoriai S. Moro, P. Rita, P. Cortez; DOI 10.24432/C5K306.
Originalių mokomųjų užrašynų autorystė paliekama dėstytojui; čia pateikiami jų pritaikymai.

Mokymas, validavimas ir testas atskirti. Normalizavimas bei kategorijų žodynai mokomi tik mokymo dalyje.
Banko `duration` pašalintas, o `target` nepatenka į įvestis. Augmentuojama tik mokant.
Slenksčiai ir galutinis modelis pasirenkami validavime, ne teste. Rodikliai nekuriami iš anksto.

## Patikros būsena

Patikrinta visų Python ląstelių sintaksė, užrašynų JSON struktūra ir reikalavimų atitikmenys.
Mokymo rezultatų nėra: parengimo aplinkoje nėra TensorFlow ir neveikia išorinių duomenų atsisiuntimas.
Visas penkias Colab programas dar reikia paleisti iš eilės, patikrinti išvestis ir išsaugoti.
Todėl tai paruoštas pritaikytas kodas su paaiškinimais, o ne jau įvykdyto eksperimento ataskaita.

## Tiesiogiai atidaryti Colab

| Užduotis | Užrašynas |
|---|---|
| 1.3.1 · Neuroninis tinklas | [Atidaryti Colab](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/1_3_1_Banko_duomenys_NN.ipynb) |
| 1.3.2 · Decision Forests | [Atidaryti Colab](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/1_3_2_Banko_duomenys_Decision_Forests.ipynb) |
| 1.4 · CNN | [Atidaryti Colab](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/1_4_CNN_Geliu_klasifikavimas.ipynb) |
| 1.5.1 · Vienas vaizdas | [Atidaryti Colab](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/1_5_1_Transfer_learning_Vienas_vaizdas.ipynb) |
| 1.5.2 · Perkėlimo mokymasis | [Atidaryti Colab](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/1_5_2_Transfer_learning_Geliu_mokymas.ipynb) |

Šiems 1.3–1.5 užrašynams Gemini API rakto nereikia. Mokymo rezultatai dar turi būti sugeneruoti paleidus Colab.
