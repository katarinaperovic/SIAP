# 📊 Predikcija Plata

## Opis projekta
Projekat predviđa **plate zaposlenih** na osnovu:
- pola  
- nivoa obrazovanja  
- naziva posla  
- godina starosti  
- godina iskustva  

Koriste se regresioni modeli: **KNN**, **Decision Tree**, **Random Forest**, **XGBoost** i **Linear Regression**.

---

## Korišćene biblioteke
python
pandas, numpy, matplotlib, seaborn  
scikit-learn, xgboost, scikit-optimize

## Modelovanje

Podaci su podeljeni na:
- **72%** trening skup  
- **8%** validacioni skup  
- **20%** test skup  

Primenjeni su **ColumnTransformer** i **Pipeline** za obradu podataka:
- `OrdinalEncoder` — kodiranje nivoa obrazovanja  
- `OneHotEncoder` — kodiranje pola i naziva posla  
- `StandardScaler` — skaliranje numeričkih vrednosti  

Ciljna promenljiva **Salary** je log-transformisana pomoću:
python
np.log1p(Salary)

