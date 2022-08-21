### Decision Tree Building Process
<figure>
    <center>
    <img src="Decision Tree.png" alt="Decision Tree" style="width:100%">
    <figcaption>Decision Tree</figcaption>
</figure>

### XGBoost Benefits
<figure>
    <center>
    <img src="XGBoost Benefits.png" alt="XGBoost Benefits" style="width:100%">
    <figcaption>XGBoost Benefits</figcaption>
</figure>

### Code for implementing XGBoost
**For Classification**
```
from xgboost import XGBClassifier

# Initialize the model
model = XGBClassifier()

model.fit(X_train, Y_train)
Y_pred = model.predict(X_test)
```

**For Regression**
```
from xgboost import XGBRegressor

# Initialize the model
model = XGBRegressor()

model.fit(X_train, Y_train)
Y_pred = model.predict(X_test)
```
- XGBoost algorithm and Deep Learning (Neural Network) algorithm is the most common robust algorithm that wins competitions in Kaggle

### Decision Tree Vs Neural Network
<figure>
    <center>
    <img src="Decision Tree Vs Neural Network.png" alt="Decision Tree Vs Neural Network" style="width:100%">
    <figcaption>Decision Tree Vs Neural Network</figcaption>
</figure>
