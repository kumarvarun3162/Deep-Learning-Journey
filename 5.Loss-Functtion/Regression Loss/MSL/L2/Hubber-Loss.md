### 🧠 Huber Loss in Neural Networks

**Huber Loss** is a **combination of MSE and MAE**.
It is designed to give the **best of both worlds**:

* Like **MSE** for small errors
* Like **MAE** for large errors

---

### 📌 Simple Idea

👉 In simple words:

> “If the error is small → use square (MSE style)”
> “If the error is big → use absolute (MAE style)”

---

### 📐 Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"L_\delta(y, \hat{y}) = \begin{cases} \frac{1}{2}(y - \hat{y})^2 & \text{if } |y - \hat{y}| \leq \delta \\ \delta(|y - \hat{y}| - \frac{1}{2}\delta) & \text{if } |y - \hat{y}| > \delta \end{cases}"}}

Where:

* ( y ) = actual value
* ( \hat{y} ) = predicted value
* ( \delta ) = threshold (decides small vs large error)

---

### 💡 How It Works

* 🔹 **Small error (≤ δ)** → behaves like **MSE**
* 🔹 **Large error (> δ)** → behaves like **MAE**

👉 This means:

* Smooth learning (like MSE)
* Less impact from outliers (like MAE)

---

### 🧾 Example (Simple Understanding)

Let δ = 1

| Error | Type Used         |
| ----- | ----------------- |
| 0.5   | MSE (small error) |
| 2     | MAE (large error) |

---

### 🎯 When Should We Use Huber Loss?

Use Huber Loss when:

#### ✅ 1. Regression Problems

* Same as MAE and MSE

#### ✅ 2. Data Has Some Outliers

* Not too many, but still present

#### ✅ 3. You Want Balanced Behavior

* Smooth training (like MSE)
* Robust to outliers (like MAE)

---

### ⚠️ When NOT to Use

Avoid Huber when:

* You want very simple implementation → use MAE or MSE
* You don’t want to tune extra parameter (δ)

---

### 🔥 Huber vs MAE vs MSE

| Feature         | MAE   | MSE          | Huber          |
| --------------- | ----- | ------------ | -------------- |
| Outliers        | Good  | Bad          | Balanced ✅     |
| Large Errors    | Equal | High penalty | Medium penalty |
| Smooth Gradient | ❌     | ✅            | ✅              |

---

### 🚀 Summary

* Huber Loss = **MSE + MAE combined**
* Uses a threshold (δ) to switch behavior
* Best for **real-world regression problems**
* Handles outliers **better than MSE** and trains **better than MAE**

---
