# **Personalized Medicine: Redefining Cancer Treatment**

[Kaggle - Personalized Medicine: Redefining Cancer Treatment](https://www.kaggle.com/competitions/msk-redefining-cancer-treatment/overview)
### **Problem statement**
In this problem we develop algorithms to classify genetic mutations based on clinical evidence (text).

### **Mapping real world problem to ML problem**
* There are nine different classes a genetic mutation can be classified on.
* Multi-Class Classification problem

### **Business objectives**
*   The cost of a mis-classification can be very high.
*   Provide the probability that each data-point belonging to each of the nine classes for better interpretation.
*   Interpretability is important. (Will be useful for Diagnosis)
*   No-strict latency requirements.

### **Performance metric**
* Cross entropy
* Confusion matrix

### **Overview of the Data set**
* **training_variants** provides the information about the genetic mutations.
* **training_text** provides the clinical evidence (text) that human experts used to classify the genetic mutations. Both are linked via the ID field.

#### **training_variants** 
> A comma separated file containing the description of the genetic mutations used for training.
* **ID** : The id of the row used to link the mutation to the clinical evidence
* **Gene** : The gene where this genetic mutation is located
* **Variation** : The aminoacid change for this mutations
* **Class** : The class (1-9) this genetic mutation has been classified into

#### **training_text**
>  A double pipe (||) delimited file that contains the clinical evidence (text) used to classify genetic mutations.
* **ID** : the id of the row used to link the clinical evidence to the genetic mutation
* **Text** : the clinical evidence used to classify the genetic mutation

**Train-Test Split:**

* We build train and test by randomly splitting in the ratio of 70:30
