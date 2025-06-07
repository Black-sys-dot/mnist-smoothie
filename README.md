# mnist-smoothie
A warm little project that teaches a model to read handwritten digits using softmax regression. Just pixels, math, and magic ✨
<br>
<br>
# 🧠 MNIST Softmax Classifier

Welcome to the **Softmax Regression Wonderland**, where a matrix of weights tries its best to understand handwritten digits (0–9). It's just some pixels, a bit of math, and a softmax function doing all the heavy lifting.

<br>

## 🪄 What does this project do?

This tiny but mighty project trains a **Softmax Regression model** on the **MNIST dataset** using pure NumPy — no TensorFlow, PyTorch, or any high-level shortcuts. The model learns to classify digits based on 28×28 grayscale images.

Yes, our little matrix learns to tell a 3 from an 8. 💪

<br>

## 📦 What's inside?

- 🔢 **One-hot encoding** for labels (because digits deserve identity too)
- 🧼 **Pixel normalization** (0–255 → 0–1 range)
- 🔁 A **251-iteration loop** to update weights (it tried hard, okay?)
- 📈 Manual **softmax math** and **gradient computation**
- 🧮 Accuracy calculated like a proud math nerd
- 💾 Model saving via `np.savetxt` (who needs `.h5` anyway?)

<br>

## 🧪 Accuracy?

On the training data:
> 🏆 **~87.4%** accuracy — no deep learning, just deep thinking.

💡 Bonus: It even skips predictions if the softmax is too unsure (confidence matters!).

<br>

<br>

## 📁 Pretrained Weights (Optional)

Already trained and tired? 🥱 No worries.

You can skip training and use the **pretrained weights and bias** included in this repo:

- `weights.csv`
- `bias.csv`

Just load them like this:

```python
import numpy as np

weights = np.loadtxt("weights.csv", delimiter=",")
bias = np.loadtxt("bias.csv", delimiter=",").reshape(1, 10)


