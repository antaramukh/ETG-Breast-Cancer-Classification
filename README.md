# ETG-Breast-Cancer-Detection

Breast Cancer Classification with Deep Learning is a Machine Learning project done as part of my Internship with Elite Techno Groups.

Scikit-Learn provides seven datasets, which they call toy datasets. These datasets are powerful and serve as a strong starting point for learning ML. Breast Cancer Wisconsin (diagnostic) dataset is one of them and the dataset we use for this project.

Breast Cancer Wisconsin (diagnostic) dataset: To diagnose cancer scans as benign (does not spread to the rest of the body) or malignant (spreads to rest of the body).

The dataset is loaded and store it into a variable called data. The load function (load_breast_cancer()) don’t return data in the tabular format. They return a Bunch object. Think of a Bunch object as Scikit-Learn’s fancy name for a dictionary.

#### Keys: 

**1. data** is all the feature data (the attributes of the scan that help us identify if the tumor is malignant or benign, such as radius, area, etc.) in a NumPy array.

**2. target** is the target data (the variable you want to predict, in this case whether the tumor is malignant or benign) in a NumPy array.

These two keys are the actual data. The remaining keys (below), serve a descriptive purpose. All of Scikit-Learn datasets are divided into data and target. data represents the features, which are the variables that help the model learn how to predict. target includes the actual labels. In our case, the target data is one column classifies the tumor as either 0 indicating malignant or 1 for benign.

**3. frame** is a DataFrame of shape (569, 31) and is only present when as_frame=True. DataFrame with data and target.

**4. feature_names** are the names of the feature variables, in other words names of the columns in data.

**5. target_names** is the name(s) of the target variable(s), in other words name(s) of the target column(s).

**6. DESCR** , short for DESCRIPTION, is a description of the dataset.

**7. filename** is the path to the actual file of the data in CSV format.

From the given information of the breast cancer dataset , we need to classify whether it is a malignant cancer or benign cancer.

Let us first look at some of the concepts to understand the project better.

### What is Deep learning?
Deep Learning is a subfield of machine learning concerned with algorithms inspired by the structure and function of the brain called artificial neural networks. Deep learning is a machine learning technique that teaches computers to do what comes naturally to humans: learn by example.

### What are artificial neural networks?
An artificial neuron network (ANN) is a computational model based on the structure and functions of biological neural networks. Information that flows through the network affects the structure of the ANN because a neural network changes - or learns, in a sense - based on that input and output.

### Keras
Keras is an API designed for human beings, not machines. Keras follows best practices for reducing cognitive load: it offers consistent & simple APIs, it minimizes the number of user actions required for common use cases, and it provides clear & actionable error messages.

For this project, we have used Keras which is a high-level Neural Networks API built on top of low level neural networks APIs like Tensorflow and Theano. There are two ways to build Keras models: sequential and functional.

**1. Sequential API:** It allows you to create models layer-by-layer for most problems. It is limited in that it does not allow you to create models that share layers or have multiple inputs or outputs. We use Sequectial model for this project.

**2. Functional API:** It is more flexible than the sequential API. It is more powerful than the sequential API in the sense branching or sharing of layers is allowed here. And also it can have multiple inputs and outputs.

### Activations
In machine learning, activation function is a special function used to find whether a specific neuron is activated or not. Basically, the activation function does a nonlinear transformation of the input data and thus enable the neurons to learn better. Output of a neuron depends on the activation function. In this project, we use relu and sigmoid function.

**relu:** Applies the rectified linear unit activation function.

**sigmoid:** Sigmoid activation function, sigmoid(x) = 1 / (1 + exp(-x)).
