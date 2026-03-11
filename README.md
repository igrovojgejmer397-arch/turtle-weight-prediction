\# Turtle Weight Prediction



\## Project Description



This project builds a machine learning model to predict the \*\*weight of sea turtles\*\* using biometric measurements collected by the TurtleCV system.



The goal is to estimate turtle mass without physically weighing the animal, which helps reduce stress and improve monitoring during rehabilitation and research.



---



\## Problem Type



Regression task.



Target variable:

\- `weight`



Features include biometric measurements such as:



\- shell length

\- shell width

\- head length

\- head width

\- flipper measurements

\- circle count

\- shell damage indicator (`shell\_crack`)



---



\## Data Processing



During preprocessing several steps were performed:



\- fixing measurement errors (values multiplied by 10)

\- handling missing values

\- removing technical columns (`id`, `timestamp`)

\- encoding the `shell\_crack` feature

\- scaling numerical features using `StandardScaler`



Dataset was split into:



\- \*\*60% training\*\*

\- \*\*20% validation\*\*

\- \*\*20% test\*\*



---



\## Models



Three regression models were trained and compared:



\- Linear Regression

\- Ridge Regression

\- Lasso Regression



Model comparison was performed using the following metrics:



\- MAE (Mean Absolute Error)

\- MAPE (Mean Absolute Percentage Error)

\- R² (Coefficient of Determination)



---



\## Results



Final model: \*\*LinearRegression\*\*



Test metrics:



\- \*\*MAE ≈ 15\*\*

\- \*\*R² ≈ 0.947\*\*



The model explains about \*\*94.7% of the variance\*\* in turtle weight and predicts mass with an average error of about \*\*15 units\*\*.



MAPE was not used for interpretation due to the presence of very small target values in the dataset.



---



\## Model Interpretation



Analysis of model coefficients shows that the most important predictors are measurements related to:



\- shell size

\- flipper length

\- head size



This is biologically consistent because turtle mass strongly correlates with body dimensions.



---



\## Technologies Used



\- Python

\- Pandas

\- NumPy

\- Scikit-learn

\- Matplotlib

\- Seaborn

\- Jupyter Notebook



---



\## Repository Structure



