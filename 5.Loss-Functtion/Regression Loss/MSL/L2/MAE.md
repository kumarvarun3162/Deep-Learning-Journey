 ## 🧠 Mean Absolute Error (MAE) Loss 

**Mean Absolute Error (MAE)** is a loss function used to measure **how much your model’s predictions differ from actual values**.

---

### 📌 Simple Idea

MAE calculates the **average of absolute differences** between:

* Actual value
* Predicted value

👉 In simple words:

> “On average, how much is my model wrong?”

---

### 📐 Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|"}}

Where:

* ( y_i ) = actual value
* ( \hat{y}_i ) = predicted value
* ( n ) = number of data points

---

### 💡 Why “Absolute” Error?

We take absolute value because:

* No negative values (distance is always positive)
* Treats all errors **equally** (no extra punishment for big errors)

---

### 🧾 Example

| Actual | Predicted | Error | Absolute Error |
| ------ | --------- | ----- | -------------- |
| 10     | 8         | 2     | 2              |
| 5      | 7         | -2    | 2              |

👉 MAE = (2 + 2) / 2 = **2**

---

### 🎯 When Should We Use MAE?

Use MAE when:

#### ✅ 1. Regression Problems

* Predicting continuous values like:

  * Prices 💰
  * Sales 📊
  * Temperature 🌡️

#### ✅ 2. When You Want Equal Importance to All Errors

* Small and large errors are treated **same**

#### ✅ 3. When Data Has Outliers

* MAE is **robust** (not сильно affected by extreme values)

---

### ⚠️ When NOT to Use MAE

Avoid MAE when:

* You want to **punish large errors more** → use MSE instead
* You need smooth gradients for faster training (MAE can be a bit slower)

---

### 🔥 MAE vs MSE (Quick Difference)

| Feature      | MAE              | MSE              |
| ------------ | ---------------- | ---------------- |
| Error Type   | Absolute         | Squared          |
| Outliers     | Less sensitive ✅ | Very sensitive ❌ |
| Large Errors | Treated equally  | Penalized more   |

---

### 🚀 Summary

* MAE = Average absolute error
* Simple and easy to understand
* Best when data has **outliers**
* Used in **regression problems**

---
