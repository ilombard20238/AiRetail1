# Retail AI — Intelligent Merchandise Identification System

Retail AI is a vision-based AI system designed to help retail stores identify merchandise **without price tags**.  
Using a camera-equipped scanner and a custom-trained AlexNet model, Retail AI instantly recognizes an item and retrieves the **correct price**, eliminating guesswork and preventing revenue loss.

---

## 📌 1. Problem Overview

Retail stores often lose money because:

- Price tags fall off or fade.
- Employees cannot identify a product quickly.
- Customers walk away when price checks take too long.
- Items are accidentally sold **below true price**, reducing profitability.
- Managers waste time searching through inventory systems manually.

**Retail AI solves these problems with instant, camera-based identification.**

---

## 💡 2. The Retail AI Solution

Retail AI provides:

- Instant merchandise identification  
- Accurate pricing  
- Confidence scoring  
- Alternative match suggestions  
- Cloud-sync functionality for updated product databases  
- Faster customer service and checkout flow  

### What the system does:
1. Employee scans or photographs the item.  
2. AI identifies the item using the trained model.  
3. System returns:
   - Product name  
   - SKU  
   - Correct price  
   - Confidence score  
4. Optional: Updates automatically from a cloud inventory database.

---

## 🧠 3. How It Works — AlexNet Model Explanation

Retail AI uses a custom-trained version of **AlexNet**, a well-known convolutional neural network (CNN).

### ➤ AlexNet Structure Summary
AlexNet contains:
- **5 Convolutional Layers** (feature extraction: edges, shapes, textures)
- **Max-Pooling Layers** (reduces spatial size & noise)
- **ReLU Activations** (fast non-linear learning)
- **Dropout Layers** (reduce overfitting)
- **3 Fully Connected Layers** (final classification)

### ➤ How AlexNet Works in THIS Project
You trained AlexNet on **6 specific items**, including:
- green Crocs  
- brown Wrangler bag  
- fancy black hat  
- (and 3 other item classes)

Each class contains:
- **20 training images**
- **20 testing images**

Instead of categorizing by type (e.g., shoes, bags), the model learns **each specific product individually**, which is ideal for price identification systems.

When an image is passed in:
1. The convolutional layers extract features from the item (color, shape, texture).
2. The network compares these features to the learned representations of your 6 items.
3. The output layer returns the **most likely item** and a confidence score.

This allows the model to identify **specific products**, not just categories.

---

## 🧪 4. Training Setup

Training performed in **Google Colab**  
- Framework: **PyTorch**  
- Model: AlexNet (modified for 6 output classes)  
- Dataset: 120 total images (20 per class)  
- Directory structure:


## Check out my website here
https://ilombard20238.github.io/websiteRetailAi/

## Poster 
https://docs.google.com/presentation/d/1ISCFmlA34qTpxsUmHuxP66P64vRglfmGC90VPO5VWE4/edit?slide=id.p#slide=id.p
