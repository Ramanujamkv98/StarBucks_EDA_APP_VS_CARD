Starbucks Payment Type Prediction (Card vs App)
Why this project?

Starbucks has been pushing app adoption for years, but not every customer is equally likely to switch from paying by card to using the app.
This project explores a simple question:

Which customers are most likely to switch from Card to App, so Starbucks can send targeted app-only promotions instead of generic offers?

What I did

I treated this as a real-world analytics problem and built an end-to-end machine learning workflow:

Explored customer demographics, spending behavior, menu preferences, and store patterns

Cleaned and transformed the data to make it model-ready

Built a logistic regression model to predict whether a customer uses Card or App

Evaluated the model using business-relevant metrics and interpreted the results to extract insights

Data & Features

Target: PaymentType (Card = 0, App = 1)

Numeric inputs:
Age, Income, BasePrice, AddOnsCost, TotalCost, SatisfactionScore

Categorical inputs (one-hot encoded):
StoreLocation, MenuCategory, DayOfWeek

How the model works

Used StandardScaler for numeric features

Used OneHotEncoder for categorical variables

Built a clean scikit-learn Pipeline with preprocessing + Logistic Regression

Split data into train/test sets with stratification to preserve class balance

Results (What stood out)

ROC-AUC: 0.962 → excellent separation between App and Card users

F1-Score: 0.88 → strong balance between precision and recall

The confusion matrix shows the model is especially good at identifying App users, which is valuable for targeting campaigns

Feature importance analysis showed that:

Add-ons cost is a strong indicator of App usage

Certain menu categories, store locations, and days of the week meaningfully influence payment behavior

Business takeaway

Instead of blasting app promotions to everyone, Starbucks could:

Target customers with high predicted probability of switching

Customize offers based on menu preference and add-on behavior

Improve conversion while reducing unnecessary discounts

Tools & Skills Used

Python, Pandas, NumPy
scikit-learn (Pipelines, Logistic Regression, ROC-AUC, F1, Confusion Matrix)
Matplotlib & Seaborn for visualization

Why this project matters

This project demonstrates my ability to:

Go from a business question → data → model → insight

Build clean, reproducible ML pipelines

Balance model performance with interpretability

Communicate results in a way that supports real decisions
