### 🧠 Binary Cross Entropy (BCE) Loss

**Binary Cross Entropy** is a loss function used when your model is solving a **binary classification problem** (only 2 classes).

👉 Examples:

* Spam vs Not Spam 📧
* Disease vs No Disease 🏥
* 0 vs 1 classification

---

### 📌 Simple Idea

👉 In simple words:

> “How close is the predicted probability to the actual label (0 or 1)?”

* If prediction is **close to correct → low loss ✅**
* If prediction is **far from correct → high loss ❌**

---

### 📐 Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"L = - \frac{1}{n} \sum_{i=1}^{n} \left[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \right]"}}

Where:

* ( y ) = actual label (0 or 1)
* ( \hat{y} ) = predicted probability (between 0 and 1)
* ( n ) = number of samples

---

### 💡 How It Works

#### Case 1: Correct Prediction ✅

* Actual = 1, Predicted = 0.9 → **Low loss**

#### Case 2: Wrong Prediction ❌

* Actual = 1, Predicted = 0.1 → **Very high loss**

👉 So, BCE **punishes wrong confident predictions heavily**

---

### 🧾 Example

| Actual | Predicted | Loss   |
| ------ | --------- | ------ |
| 1      | 0.9       | Low ✅  |
| 1      | 0.2       | High ❌ |
| 0      | 0.1       | Low ✅  |
| 0      | 0.8       | High ❌ |

---

### 🎯 When Should We Use BCE?

Use Binary Cross Entropy when:

#### ✅ 1. Binary Classification Problems

* Only **2 classes (0 or 1)**

#### ✅ 2. Output Layer Uses Sigmoid

* Because sigmoid gives output between **0 and 1 (probability)**

#### ✅ 3. You Need Probabilistic Output

* Model predicts **confidence/probability**

---

### ⚠️ When NOT to Use BCE

Avoid BCE when:

* You have **more than 2 classes** → use *Categorical Cross Entropy*
* Output is not probability (no sigmoid)

---

### 🔥 Why BCE is Better than MSE for Classification?

| Feature  | MSE        | BCE               |
| -------- | ---------- | ----------------- |
| Task     | Regression | Classification ✅  |
| Output   | Any value  | Probability (0–1) |
| Learning | Slow       | Fast & accurate ✅ |

👉 BCE works better because it is designed for **probabilities**, not distances.

---

### 🚀 Summary

* Used for **binary classification**
* Works with **sigmoid activation**
* Measures difference between **true label & predicted probability**
* Punishes wrong predictions strongly

---
