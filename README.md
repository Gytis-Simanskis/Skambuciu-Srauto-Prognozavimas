# Skambučių Srauto Prognozavimas

Bakalauro baigiamojo darbo programinis kodas. Repozitorijoje pateikiami keturių prognozavimo modelių (SARIMAX, XGBoost, GRU bei hibridinio ansamblio) Jupyter kodo failai ir pavyzdinis duomenų rinkinys. Tyrimo tikslas – palyginti skirtingų laiko eilučių prognozavimo algoritmų efektyvumą.

## Repozitorijos struktūra

- **`Notebooks/`** – Aplankas, kuriame yra visi Jupyter kodo failai:
  - `SARIMAX_modelis.ipynb` – Tradicinio statistinio SARIMAX modelio specifikacijos, treniravimo ir vertinimo kodas.
  - `XGBoost_modelis.ipynb` – Sprendimų medžių ansamblio (XGBoost) kodas, apimantis požymių inžineriją ir hiperparametrų optimizavimą naudojant *Optuna*.
  - `GRU_modelis.ipynb` – Giliojo mokymosi rekurentinio neuroninio tinklo (GRU) architektūros, duomenų normalizavimo ir mokymo kodas.
  - `Hibridinis_modelis.ipynb` – Dviejų lygmenų *Stacking* ansamblio kodas, apjungiantis bazinių modelių prognozes taikant neneigiamų mažiausiųjų kvadratų (NNLS) algoritmą.
- **`Data/`** – Aplankas su duomenimis:
  - `duomenys_pavyzdys.csv` – Pavyzdinis skambučių srautų duomenų rinkinys, skirtas kodo veikimui pademonstruoti ir testuoti.
- **`requirements.txt`** – Faile pateikiamos visos projektui naudotos bibliotekos ir tikslios jų versijos.

## Duomenų privatumas ir anonimizavimas

**Svarbu:** Siekiant užtikrinti finansų institucijos konfidencialumą, `Data/` aplanke pateikiami duomenys yra anonimizuoti. Nors bendra duomenų struktūra, laiko dinamika ir sezoniškumas yra pilnai išlaikyti (tam, kad juos būtų galima sėkmingai naudoti modelių mokymui ir testavimui), absoliučios skaitinės reikšmės skiriasi nuo realių faktinių srautų.

Duomenų transformacijai atlikti kiekvienam stebiniui buvo pritaikyta ši „Excel“ formulė (kur X ir Y yra atsitiktinai parinkti sveikieji skaičiai):
```excel
=RANDBETWEEN(MAX(1; B2 - X); B2 + Y)
