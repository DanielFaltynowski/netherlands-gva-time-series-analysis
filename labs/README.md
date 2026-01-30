# Laborarory 01: GVA Data Collection, Trend and Seasonality Analysis

Download data on **gross value added (GVA)** for the Netherlands from the [**Eurostat**](https://ec.europa.eu/eurostat) website. Using **Excel**, visualize the change in GVA over time from the **first quarter of 2015 to the second quarter of 2025**.

Next, by performing appropriate **macroeconomic calculations**, remove the **linear trend** from the data.

Finally, define the **seasonality** of the time series for the given data and, using appropriate macroeconomic calculations, remove the **seasonal component** from the time series. **Describe the results.**

<br>

# Laboratory 02: Chain Indices and Constant Price Calculation

Download data on **gross value added (GVA)** for the **Netherlands** from the [**Eurostat**](https://ec.europa.eu/eurostat) website in **constant prices (reference year 2020)**.

Next, using the dataset developed in the **previous laboratories**, calculate **GVA in nominal prices** for the years **2016** and **2024**.

Then, based on:
- GVA in **constant prices (2020)** obtained from Eurostat, and  
- GVA in **nominal prices** for **2016** and **2024**,

calculate **GVA in constant prices** for the years **2016** and **2024** (with **2020 as the base year**).

Finally, enter the resulting data into your **Laboratory 01 project** and interpret the differences between the obtained time series, focusing on the impact of price changes.

<br>

# Laboratory 03: Model Estimation with Linear, Power, and Exponential Functions

For the dataset of GVA in **nominal prices**, use **Excel** and the **least squares method** to estimate the parameters of a **linear, power, and exponential model**, including an analysis of the **statistical significance of the model parameters**. Then, visualize the fitted models.  

Compare your results with those obtained using the **Data Analysis ToolPak**. Calculate the **rate of change** (first derivative) and the **growth pace** (percentage change) for each fitted model to analyze the dynamics of GVA over time.

Finally, select the model that exhibits the **smallest residual variance** as the best-fitting model and interpret the results in terms of GVA growth trends.


<br>

# Laboratory 04: Advanced GVA Modeling: Quadratic, and Logistic Models

**Laboratory 04** is a continuation of the previous laboratory work, focusing on the **modeling of Gross Value Added (GVA)**. In this exercise, you are required to estimate and fit **quadratic and logistic models** to the Netherlands GVA dataset. 

For each model, perform a thorough analysis of the **goodness-of-fit**, including the **residual variance**, **parameter significance**, and other relevant diagnostic measures. Visualize the fitted models to assess how well they capture the trends in the data.

Finally, compare the models and **select the one with the smallest residual variance**, as it represents the best approximation of the observed GVA dynamics. Additionally, provide an interpretation of the selected model in the context of economic trends and discuss its potential implications for forecasting and policy analysis.

<br>

# Laboratory 05: Structural Breaks Analysis and Model Refinement

In the previous **Laboratory 04**, the best-fitting model describing the **time series of Gross Value Added (GVA) for the Netherlands** was selected. Based on this model choice, input the appropriate data into **Gretl** and visualize the model.

You will likely observe a **structural break** in the first quarter of 2020. However, if the break appears at a different point in the data, select that point for further analysis. Conduct a **Chow test** to examine the significance of the structural break in 2020-Q1 and at any other points that appear suspicious.

For the time points identified as structural breaks, apply a **model transformation** method (e.g., a **dummy variable approach**), where for $t < k$ the model remains unchanged, and for $t \geq k$ the relevant variable is multiplied by a dummy indicator $d_1 * t_{d_1}$. Visualize the transformed model to observe the effect of the break.

Next, assess the **statistical significance of the parameters** for each model. Then, construct a **third model** using only the **statistically significant parameters** from the second model (which includes the structural break).

Finally, compare all three models, select the **best-fitting model**, and provide an interpretation of its results. Additionally, calculate and analyze the **growth rate** and **pace of change** for the selected model.

<br>

# Laboratory 06: Seasonal Dummies and Autocorrelation Analysis

Introduce **seasonal dummy variables** to the GVA model and check for **autocorrelation** in residuals for lags 1–4 using the **Breusch-Godfrey test**. Next, remove statistically insignificant variables and re-estimate the model, again testing for autocorrelation. Finally, replace seasonal dummies with **alternative indicators**, assess parameter significance and  select the best-fitting model.

<br>

# Laboratory 07: Autoregressive and Mixed Model Analysis of GVA

Using the **Gross Value Added (GVA) time series for the Netherlands**, estimate a **pure autoregressive (AR) model** including multiple lags of the dependent variable and assess its statistical properties.

Evaluate the model in terms of:
- **parameter significance**,  
- **residual autocorrelation** (Breusch–Godfrey test),  
- **parameter stability** (CUSUM test),  
- **overall model adequacy** and suitability for forecasting.

Next, construct a **mixed (structural–autoregressive) model** by combining the autoregressive structure with the best structural model obtained in previous laboratories. Analyze its statistical properties and compare it with the pure autoregressive model.

Finally, compare both models with respect to **stability, parsimony, goodness-of-fit, and forecasting reliability**, select the **best-performing specification**, and provide an **economic and econometric interpretation** of the results, including a discussion of model limitations.
