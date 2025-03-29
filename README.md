# Interpreting Deep Learning in Satellite Imagery 🌍🛰️  
**An Application of Explainable AI (XAI)**  

> **Full text available on my [ResearchGate profile](https://www.researchgate.net/publication/380999127_Satellite_Image_Classification_An_Application_of_Convolutional_Neural_Networks_Transfer_Learning_and_Explainable_AI_XAI#fullTextFileContent)** 
>
>  📄 or, [download the full report PDF](./Full-Report.pdf)

---

This project explores how deep learning models perceive satellite images—and how we can interpret those decisions using **Integrated Gradients**.  

By combining **CNNs**, **transfer learning**, and **XAI techniques**, the model classifies land types from aerial images and reveals *what it’s actually looking at* when it makes decisions.
> 🔍 For full methodology, background, model architecture, and discussion of results, see the [full report.](./Full-Report.pdf)

The final classifiers achieved:  
- **99.4% accuracy** on the 7-class general land type classifier  
- **99.5% accuracy** on the 35-class fine-grained classifier

---

## Example Visualizations

Below are examples of Integrated Gradients attributions for correctly and incorrectly classified satellite images.  
Brighter red areas show which pixels contributed most to the model’s prediction.

The **first image** is the *only misclassified example* in the test set.  
The rest were predicted correctly.

<div style="display: flex; gap: 10px; overflow-x: auto;">
  <img src="gallery/images/incorrect.png" width="400"/>
  <img src="gallery/images/3.png" width="400"/>
  <img src="gallery/images/5.png" width="400"/>
  <img src="gallery/images/12.png" width="400"/>
</div>

---

## Notebooks

Two models were developed and trained using the same XAI pipeline:

- 🏷️ [7-Class Classifier](./notebooks/7-Class-Classifier.ipynb)  
  Groups satellite land types into general categories (e.g., *urban*, *water*, *woodland*)

- 🏷️ [35-Class Classifier](./notebooks/35-Class-Classifier.ipynb)  
  A fine-grained classifier with detailed subcategories (e.g., *river*, *shrubland*, *ocean*)

---

## Full Attribution Gallery

Explore over 40 attribution maps from the test set:  
👉 [Open the full scrollable gallery](./gallery/gallery.md)

---

## 🛠️ Tools & Libraries

- Python, PyTorch, torchvision
- Captum (for Integrated Gradients)
- WandB (for training logs & dashboard)
- scikit-learn, matplotlib, pandas
