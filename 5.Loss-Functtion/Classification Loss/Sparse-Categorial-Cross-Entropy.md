### 🧠 Sparse Categorical Cross Entropy (SCCE)

**Sparse Categorical Cross Entropy** is a loss function used for **multi-class classification**, just like Categorical Cross Entropy (CCE)…
👉 but with a simpler way of giving labels.

---

### 📌 Simple Idea

👉 In simple words:

> “Instead of giving labels in one-hot format, just give the class number.”

---

### 🔄 Difference from CCE

| Type                             | Label Format        |
| -------------------------------- | ------------------- |
| Categorical Cross Entropy        | One-hot → [0, 1, 0] |
| Sparse Categorical Cross Entropy | Integer → 1         |

---

### 📐 Formula

👉 Internally, it works almost the same as CCE:

genui{"math_block_widget_always_prefetch_v2":{"content":"L = - \log(\hat{y}_{y})"}}

Where:

* ( y ) = actual class index
* ( \hat{y}_{y} ) = predicted probability of correct class

---

### 💡 How It Works

#### Example (3 classes: Cat, Dog, Car)

* Actual label:

  * CCE → [0, 1, 0]
  * SCCE → 1

* Predicted:

  * [0.1, 0.7, 0.2]

👉 Loss = depends only on **0.7 (correct class probability)**

---

### 🧾 Example

| Actual  | Predicted       | Loss   |
| ------- | --------------- | ------ |
| 1 (Dog) | [0.1, 0.7, 0.2] | Low ✅  |
| 1 (Dog) | [0.6, 0.2, 0.2] | High ❌ |

---

### 🎯 When Should We Use SCCE?

Use Sparse Categorical Cross Entropy when:

#### ✅ 1. Multi-Class Classification

* More than 2 classes

#### ✅ 2. Labels Are Integers

* Example:

  * Cat = 0, Dog = 1, Car = 2

#### ✅ 3. Want Simpler Data Handling

* No need to convert to one-hot encoding

---

### ⚠️ When NOT to Use

Avoid SCCE when:

* Labels are already one-hot encoded → use CCE
* Multi-label classification → use BCE

---

### 🔥 SCCE vs CCE

| Feature     | CCE             | SCCE             |
| ----------- | --------------- | ---------------- |
| Labels      | One-hot encoded | Integer labels ✅ |
| Memory      | More            | Less ✅           |
| Performance | Same            | Same             |

👉 Both give **same results**, only label format is different!

---

### 🚀 Summary

* Used for **multi-class classification**
* Works with **Softmax activation**
* Takes **integer labels (no one-hot needed)**
* Simpler and memory efficient

---

