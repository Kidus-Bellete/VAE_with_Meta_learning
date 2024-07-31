### FAVAE Anomaly Detection and Localization with MAML Meta-Learning

---

#### Overview

This repository implements an anomaly detection and localization system using a Variational Autoencoder (VAE) enhanced with Model-Agnostic Meta-Learning (MAML). The project includes modules for data preprocessing, model training, and evaluation.

---

#### Table of Contents

- [Overview](#overview)
- [Directory Structure](#directory-structure)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Key Scripts](#key-scripts)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

---

#### Directory Structure

```
FAVAE-anomaly-detection-localization with meta learning/
│
├── datasets/
│   ├── mvtec.py
│   └── preprocessing.py
│
├── imgs/
│   ├── pic1.jpg
│   ├── pic2.jpg
│   ├── pic3.jpg
│   └── pic4.jpg
│
├── models/
│   ├── VAE.py
│   ├── MAML.py
│   └── __init__.py
│
├── func.py
├── test.py
├── train.py
├── meta_train.py
└── utils.py
```

---

#### Setup Instructions

1. **Clone the Repository**

    ```sh
    git clone <repository-url>
    cd FAVAE-anomaly-detection-localization
    ```

2. **Install Dependencies**

    Ensure you have Python 3.x installed. Install the required Python packages using:

    ```sh
    pip install -r requirements.txt
    ```


3. **Prepare Dataset**

    Ensure your dataset is organized in the appropriate structure as required by the scripts in the `datasets/` directory.

---

#### Usage

1. **Preprocessing Data**

    Run the preprocessing script to prepare your data for training:

    ```sh
    python datasets/preprocessing.py
    ```

2. **Training the VAE Model**

    Train the Variational Autoencoder model using:

    ```sh
    python train.py --obj bottle --do_aug
    ```

3. **Training with MAML Meta-Learning**

    Train the model using MAML for better generalization across different tasks:

    ```sh
    python meta_train.py --obj bottle --do_aug
    ```

4. **Testing the Model**

    Evaluate the model's performance on the test data:

     -  Download the trained model from the provided Google Drive link.
     +  Replace the placeholder in test.py with the path to the downloaded model.
     * Run the following command, specifying the object type and the path to the checkpoint file:

    ```sh
    python test.py --obj pill --checkpoint path_to_model_checkpoint.pt

    ```

---

#### Key Scripts

- **datasets/mvtec.py**: Functions specific to handling the MVTec dataset.
- **datasets/preprocessing.py**: Script for preprocessing dataset images.
- **models/VAE.py**: Definition of the Variational Autoencoder model architecture.
- **models/MAML.py**: Implementation of the MAML algorithm for meta-learning.
- **train.py**: Script for training the VAE model.
- **meta_train.py**: Script for training the model using MAML.
- **test.py**: Script for testing the trained model.
- **func.py**: Utility functions used across various scripts.
- **utils.py**: Additional utility functions for model and data handling.

---

#### Examples

Include sample images and results in the `imgs/` directory to visualize the anomaly detection and localization results.

---

#### Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

For major changes, please open an issue first to discuss what you would like to change.

---

#### License

1. Kidus Dagnaw 

2. Abel Abebe

---

Feel free to customize and expand upon this README based on your specific project details and requirements.
