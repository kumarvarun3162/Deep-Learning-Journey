### 🧠 Categorical Cross Entropy (CCE) Loss

**Categorical Cross Entropy** is a loss function used for **multi-class classification problems** (more than 2 classes).

👉 Examples:
- Classifying images: Cat 🐱 / Dog 🐶 / Car 🚗  
- Digit recognition: 0–9  
- News classification: Sports / Politics / Tech  

---

### 📌 Simple Idea

👉 In simple words:  
> “How close is the predicted probability distribution to the actual class?”

- Model gives probabilities for all classes  
- Only one class is correct → we check how much probability it got  

---

### 📐 Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"L = - \\sum_{i=1}^{C} y_i \\log(\\hat{y}_i)"}}

Where:  
- \( C \) = number of classes  
- \( y_i \) = actual label (one-hot encoded: 0 or 1)  
- \( \hat{y}_i \) = predicted probability  

---

### 💡 How It Works

- Actual label is **one-hot encoded**
  - Example (3 classes):  
    - Dog → [0, 1, 0]

- Model predicts probabilities:
  - [0.1, 0.7, 0.2]

👉 Loss focuses only on the **correct class probability**

---

### 🧾 Example

| Actual (One-hot) | Predicted | Loss |
|------------------|----------|------|
| [0,1,0] | [0.1, 0.7, 0.2] | Low ✅ |
| [0,1,0] | [0.6, 0.2, 0.2] | High ❌ |

👉 If correct class gets **high probability → low loss**

---

### 🎯 When Should We Use CCE?

Use CCE when:

#### ✅ 1. Multi-Class Classification
- More than **2 classes**

#### ✅ 2. Single Correct Class
- Only **one correct label per sample**

#### ✅ 3. Output Layer Uses Softmax
- Softmax converts outputs into **probabilities that sum to 1**

---

### ⚠️ When NOT to Use CCE

Avoid CCE when:
- Binary classification → use BCE  
- Multi-label classification (multiple correct labels) → use Binary Cross Entropy  

---

### 🔥 CCE vs BCE

| Feature | BCE | CCE |
|--------|-----|-----|
| Classes | 2 | More than 2 ✅ |
| Output | Sigmoid | Softmax ✅ |
| Labels | 0/1 | One-hot encoded |

---

### 🚀 Summary

- Used for **multi-class classification**  
- Works with **Softmax activation**  
- Compares **true class vs predicted probabilities**  
- Lower loss = better prediction  
