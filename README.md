In this project, I focused on implementing and evaluating Support Vector Machines (SVM) for classification tasks. I tackled several key challenges, starting with binary classification, where I implemented an SVM from scratch using the Sequential Minimal Optimization (SMO) algorithm. This allowed me to solve the quadratic programming problem and find the optimal decision boundary that separates the classes with maximum margin. I used both linear and polynomial kernels to classify the data and compared my implementation with Scikit-learn’s LinearSVC, ensuring that my custom model aligned well with industry-standard libraries.

Next, I explored non-linear SVMs using a polynomial kernel, which transformed the data into higher dimensions, allowing me to classify data that was not linearly separable. I also addressed the challenge of ensuring that the kernel matrix was positive semi-definite, which is crucial for the optimization process in SVMs.

Additionally, I extended my work to handle multiclass classification using the One-vs-Rest (OvR) strategy. I trained multiple binary classifiers for each class and selected the class with the highest decision function score. I compared the performance of my custom multiclass SVM with Scikit-learn’s OvR implementation, testing both linear and polynomial kernels.

My approach is efficient because I implemented SVMs from scratch, gaining full control over the training process and kernel selection. This allowed me to deeply understand the algorithm’s workings while also comparing its performance with well-established models. I also incorporated regularization to avoid overfitting and tested different kernels to ensure my model could handle both linearly and non-linearly separable data. By validating my model against Scikit-learn and using grid search for hyperparameter tuning, I ensured my solution was both accurate and efficient.

**Outputs:**
These are initial values:
[ 0.6837343 -0.57983761] 0.262312585114426
weights=[ 0.6837343 -0.57983761] b=0.262312585114426
coef_=[[ 0.79601822 -0.72590071]] intercept=[0.01429259]

The below are the values i got:
[ 0.60648785 -1.07014398] 0.11374000567862574
weights=[ 0.60648785 -1.07014398] b=0.11374000567862574
coef_=[[ 0.8190781 -0.65725882]] intercept=[-0.03861194]
So the graphs are generated accordingly.

Below is the output when the kernel is non positive semi definite. output:
The kernel matrix is not positive semidefinite.
Eigenvalues: [ 1.40000000e+01 2.64152997e-16 -4.59474257e-16]

**1. Non linear SVM:**
Below are the accuracies and corresponding plots.

<img width="508" alt="image" src="https://github.com/user-attachments/assets/8d7f0f6a-8021-4771-bc14-881e4f39bd47">

**2. Multiclass SVM:**
Below are the accuracies:
Custom MultiSVM(Linear) accuracy: 0.96 Custom MultiSVM(Poly) accuracy: 0.91 Sklearn OneVsRest(Linear) accuracy: 0.96 Sklearn OneVsRest(Poly) accuracy: 0.91
