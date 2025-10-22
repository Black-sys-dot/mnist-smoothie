# 🍺 MNIST Smoothie  

![Python](https://img.shields.io/badge/Python-3.10-blue)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-orange)
![MNIST](https://img.shields.io/badge/Dataset-MNIST-lightgrey)
![Model](https://img.shields.io/badge/Model-Softmax%20Regression-green)
![Status](https://img.shields.io/badge/Status-Trained%20~87%25-success)

---

## 🧠 MNIST Softmax Classifier

Welcome to the **Softmax Regression Wonderland**,  
where a humble matrix of weights tries its best to understand handwritten digits (0–9).  
It’s just some pixels, a bit of math, and a softmax function doing all the heavy lifting. ✨  

---

## 🪄 What Does This Project Do?

This tiny but mighty project trains a **Softmax Regression model** on the **MNIST dataset** using pure **NumPy** —  
no TensorFlow, no PyTorch, no excuses.  

The model learns to classify digits from **28×28 grayscale images**,  
and honestly… it does a pretty solid job for something built from scratch. 💪  

---

## 📦 What’s Inside?

- 🔢 **One-hot encoding** for labels (because digits deserve individuality too)  
- 🧼 **Pixel normalization** → 0–255 squished into 0–1  
- 🔁 **251 training loops** — it’s trying its best, okay?  
- 📈 **Manual softmax** and gradient calculations (math gang rise up 🧮)  
- 💾 Model saving via `np.savetxt` (who needs `.h5` anyway?)  

---

## 🧪 Accuracy?

On the training data:  
> 🏆 **~87.4% accuracy** — no deep learning, just deep thinking.  

💡 Bonus feature:  
If the model’s softmax confidence is too low, it *skips* predictions.  
Because even AI knows when to say, “I don’t know, bro.” 🤷‍♂️  

---

## 📁 Pretrained Weights (Optional)

Already trained and tired? 🥱  
No worries — pretrained weights are here to save your neurons.  

You’ll find:  
- `weights.csv`  
- `bias.csv`  

Load them like this:
```python
import numpy as np

weights = np.loadtxt("weights.csv", delimiter=",")
bias = np.loadtxt("bias.csv", delimiter=",").reshape(1, 10)
