# Skambuciu-Srauto-Prognozavimas

Bakalauro baigiamojo darbo programinis kodas. Repozitorijoje pateikiami keturių prognozavimo modelių (SARIMAX, XGBoost, GRU bei hibridinio ansamblio) Jupyter kodo failai ir pavyzdinis duomenų rinkinys. Tyrimo tikslas – palyginti skirtingų laiko eilučių prognozavimo algoritmų efektyvumą.

## Repozitorijos turinys

- **`1_SARIMAX_modelis.ipynb`** – Tradicinio statistinio SARIMAX modelio specifikacijos, treniravimo ir vertinimo kodas.
- **`2_XGBoost_modelis.ipynb`** – Sprendimų medžių ansamblio (XGBoost) kodas, apimantis požymių inžineriją ir hiperparametrų optimizavimą naudojant *Optuna*.
- **`3_GRU_modelis.ipynb`** – Giliojo mokymosi rekurentinio neuroninio tinklo (GRU) architektūros, duomenų normalizavimo ir mokymo kodas.
- **`4_Hibridinis_modelis.ipynb`** – Dviejų lygmenų *Stacking* ansamblio kodas, apjungiantis bazinių modelių prognozes taikant neneigiamų mažiausiųjų kvadratų (NNLS) algoritmą.
- **`duomenys_pavyzdys.csv`** – Pavyzdinis skambučių srautų duomenų rinkinys, skirtas kodo veikimui pademonstruoti ir testuoti. **Svarbu:** Šiame faile rodoma tik bendra duomenų struktūra. Jame esantys skaičiai nėra realūs faktiniai tyrime naudoti duomenys – jie sugeneruoti atsitiktine tvarka (naudojant *random* funkcijas) tik kaip demonstracinis pavyzdys.

## Programinė įranga ir priklausomybės

Visi skaičiavimai atlikti `Python 3.11` aplinkoje. Pagrindinės naudotos bibliotekos:
- **Duomenų apdorojimui:** `pandas`, `numpy`, `scikit-learn`
- **Modeliavimui:** `statsmodels`, `pmdarima` (SARIMAX), `xgboost`, `optuna` (XGBoost), `tensorflow`, `keras` (GRU), `scipy` (NNLS)
- **Vizualizacijoms:** `matplotlib`, `seaborn`

Šio darbo programinis kodas buvo kuriamas ir testuojamas **Visual Studio Code (VSCode)** aplinkoje. Norint peržiūrėti ar atkurti rezultatus, failus galima naudoti toje pačioje VSCode aplinkoje (su įdiegtu Jupyter plėtiniu) arba atidaryti per standartines *Jupyter Notebook*, *JupyterLab* ar *Google Colab* platformas.
