# 🧠 Mean Square Loss (MSE)

**Mean Square Loss (MSE)** is one of the most commonly used loss functions in neural networks. It helps us measure **how wrong our model’s predictions are**.

---

## 📌 Simple Idea

MSE calculates the **average of the squared differences** between:

* **Actual value (true output)**
* **Predicted value (model output)**

👉 In simple words:

> “How far is my prediction from the real answer?”

---

## 📐 Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2"}}

Where:

* ( y_i ) = actual value
* ( \hat{y}_i ) = predicted value
* ( n ) = number of data points

---

## 💡 Why “Square” the Error?

We square the error because:

* Negative and positive errors both become **positive**
* Larger mistakes get **more punishment** (important!)

---


## 🎯 When Should We Use MSE?

Use MSE when:

### ✅ 1. Regression Problems

* Predicting **continuous values**

  * House prices 🏠
  * Temperature 🌡️
  * Stock prices 📈

### ✅ 2. When Large Errors Matter More

* Because squaring gives **higher penalty to big mistakes**

### ✅ 3. When Data is Clean (Less Outliers)

* MSE is sensitive to outliers (extreme values)

---

## ⚠️ When NOT to Use MSE

Avoid MSE when:

* You are solving **classification problems** (use cross-entropy instead)
* Your data has **too many outliers**

---

## 🚀 Summary

* MSE = Average squared difference between actual & predicted values
* Simple, powerful, widely used
* Best for **regression tasks**
* Punishes large errors more

