# ND1 · 1.3–1.5

**Liutauras Turauskis · DIPf-24**

Visos penkios dalys sujungtos į vieną užrašyną **[ND1_1_3_1_5.ipynb](ND1_1_3_1_5.ipynb)**.

[![Atidaryti Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Laran20/DI-pagrista-programavimo-klaidu-analizes-sistema/blob/main/ND1_1_3_1_5/ND1_1_3_1_5.ipynb)

| Skyrius | Turinys |
|---|---|
| 1.3.1 | Banko duomenų neuroninis tinklas: kategorijos, normalizavimas, mokymas ir testas |
| 1.3.2 | TensorFlow Decision Forests: miškas, OOB grafikai, medis, svarba ir palyginimas su NN |
| 1.4 | Gėlių CNN ir MLP; filtrai, požymių žemėlapiai ir rankinė koreliacija |
| 1.5.1 | Nuotraukos klasifikavimas, iškarpa, objektų aptikimas ir semantinis segmentavimas |
| 1.5.2 | Perkėlimo mokymasis: užšaldyta bazė, augmentavimas, nauja galva ir fine-tuning |

## Paleidimas

1. Atidaryti bendrą užrašyną per Colab mygtuką.
2. Vaizdų mokymui pasirinkti **Runtime → Change runtime type → T4 GPU**, jei prieinamas.
3. Naujoje sesijoje pasirinkti **Runtime → Run all**. Vykdyti nuo pradžios: skyriai naudoja bendrus paruoštus duomenis.
4. Patikrinti išvestis ir išsaugoti užrašyną su jomis per **File → Save a copy in GitHub**, tuo pačiu failo keliu.

Gemini API rakto ir papildomų įvesties failų nereikia. Banko duomenys atsisiunčiami vieną kartą,
gėlių duomenys – vieną kartą. TFDF vykdomas izoliuotoje Python 3.12 / TensorFlow 2.19 Linux aplinkoje;
Colab branduolio tarp skyrių perkrauti nereikia. Duomenų ir modelių atsisiuntimui reikia interneto,
laiko ir laisvos atminties; HRNet modelis didesnis.

Eksportai atskirti: `rezultatai/1_3/`, `rezultatai/1_4/`, `rezultatai/1_5_1/`, `rezultatai/1_5_2/`.
Norint juos išlaikyti, iki Colab sesijos pabaigos atsisiųsti atitinkamus katalogus.

## Duomenys ir pavyzdžiai

Pasirinkti vieši rinkiniai, skirtingi nuo dėstytojo pavyzdžiuose naudotų:
[UCI Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)
(taip pat [Kaggle](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)) ir
[TensorFlow Flowers Photos](https://www.tensorflow.org/tutorials/load_data/images).
Banko duomenų autoriai S. Moro, P. Rita, P. Cortez; DOI 10.24432/C5K306, CC BY 4.0.
Nuotraukų autoriai ir CC BY licencijos pateikti duomenų archyvo `LICENSE.txt`.

Pritaikyta pagal dėstytojo `AdventureWorksDW_NN.ipynb`, `AdventureWorksDW_Decision_Forests.ipynb`,
`cnn.ipynb`, `cnn_One_Image.ipynb` ir `cnn_Transfer_learning.ipynb`. Eiga ir pakeitimai paaiškinti
prie atitinkamo kodo. Ankstesnis DI programavimo klaidų analizės darbas lieka atskiras.

## Patikros būsena

Patikrinta sujungto užrašyno JSON struktūra, Python ląstelių ir vidinio TFDF skripto sintaksė,
bendrų funkcijų priklausomybės ir pakartotinio duomenų naudojimo eiga.
**Visas TensorFlow mokymas dar nepaleistas:** parengimo aplinkoje nėra tinkamos vykdymo aplinkos
ir neveikia bibliotekų bei duomenų atsisiuntimas. Išvestys ir rodikliai neįrašyti iš anksto.
Prieš pateikiant darbą reikia Colab paleisti visą užrašyną, patikrinti ir išsaugoti tikras išvestis.
