This project implements a hybrid quantum-classical machine learning model for breast cancer detection, combining quantum circuits (PennyLane) with classical ML (SVM, Scikit-Learn). The objective is to leverage Quantum Machine Learning (QML) for real-world medical diagnosis tasks and benchmark it against classical approaches.

Key Features

Dataset Integration: Merged Wisconsin Breast Cancer dataset and Curated Pathology dataset with 10 diagnostic features.

Data Preprocessing: Standardized features, handled missing values, and created train/test splits for robust evaluation.

Quantum Circuit Design: Used StronglyEntanglingLayers in PennyLane with multiple qubits (equal to number of features). Encoded classical patient features into qubit states via RY rotations. Computed Pauli-Z expectation values as output features. Hybrid Model: Constructed a Quantum-Classical Hybrid Model with parameterized quantum layers + classical sigmoid activation. Trained using Adam Optimizer with binary cross-entropy loss.

Classical Benchmark: Built a Support Vector Machine (SVM) classifier for comparison.

Performance Profiling: Leveraged Python’s cProfile to optimize circuit execution and training speed.

Results: Quantum Model Accuracy: ~92% on test data. Classical SVM Accuracy: ~95% on same test split. Demonstrates that QML is competitive with classical ML, especially as qubit scalability improves.

Tools & Technologies:

Languages & Libraries: Python, PennyLane, Scikit-Learn, NumPy, Pandas, Matplotlib, Seaborn.
Quantum Frameworks: PennyLane (default.qubit, lightning.qubit backend).
ML Frameworks: Scikit-Learn (SVM, preprocessing).
