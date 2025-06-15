# 🔬 Blood Group Detection Using Fingerprint Image Processing

This project presents a novel deep learning approach for blood group detection using fingerprint images. Leveraging convolutional neural networks (CNNs), the model identifies blood types (A, B, AB, O – including Rh factors) by analyzing ridge patterns in fingerprint images.

---

## 🚀 Key Features

- 🧠 CNN-based model trained on a labeled dataset of fingerprint images
- 📈 High accuracy, precision, and recall in blood group classification
- 🧪 Uses data augmentation to improve model generalization
- ⚡ Fast, non-invasive alternative to traditional chemical-based tests
- 🏥 Ideal for point-of-care diagnostics and resource-limited settings

---

## 🔍 Technologies Used

- **Python**
- **PyTorch**
- **OpenCV**
- **Flask**
- **NumPy & Pandas**

---

## 🚀 How to Set Up and Run This Project

To get a local copy up and running, follow these simple steps.

### Prerequisites

You will need to have Python 3.x and Pip installed on your system.

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/CodewithShaaz/AI-Bloodgroup-Analyzer-using-fingerprint.git](https://github.com/CodewithShaaz/AI-Bloodgroup-Analyzer-using-fingerprint.git)
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd AI-Bloodgroup-Analyzer-using-fingerprint
    ```

3.  **Install the required libraries:**
    First, ensure you have a `requirements.txt` file in your repository. If not, create one by running `pip freeze > requirements.txt` in your terminal and pushing it to GitHub. Then, run the following command:
    ```sh
    pip install -r requirements.txt
    ```

4.  **Download the Pre-trained Model:**
    The trained model is not stored on GitHub. Please download it from the link below and place the `Model.pth` file inside the `Model/` directory.
    > **Download Link:** [**<-- PASTE YOUR GOOGLE DRIVE/DROPBOX LINK HERE**]

### Usage

1.  **Navigate to the application folder:**
    ```sh
    cd Code
    ```

2.  **Run the Flask application:**
    ```sh
    python app.py
    ```

3.  Open your web browser and go to the address shown in your terminal (usually `http://127.0.0.1:5000`) to use the application.

---

## 📁 Dataset

The model was trained on a curated dataset of fingerprint images tagged with corresponding blood group labels:
- **Blood Types:** A, B, AB, O
- **Rh Factors:** Positive (+), Negative (−)

---

## 📊 Results

The trained CNN demonstrates high classification accuracy and robustness, showing that fingerprint ridge patterns can serve as biometric indicators for blood group detection.

---

## 📌 Future Scope

- Expand dataset diversity for improved generalization
- Explore hybrid or ensemble models
- Integration into mobile or embedded systems for real-world application

---

## 🖼️ Demo Images

<p align="center">
  <img src="images/Screenshot%202025-04-24%20013628.png" width="800" alt="Sample 1"/>
  <img src="images/Screenshot%202025-04-24%20013646.png" width="800" alt="Sample 2"/>
  <img src="images/Screenshot%202025-04-24%20013657.png" width="800" alt="Sample 3"/>
  <img src="images/Screenshot%202025-04-24%20013716.png" width="800" alt="Sample 4"/>
  <img src="images/Screenshot%202025-04-24%20013730.png" width="800" alt="Sample 5"/>
  <img src="images/Screenshot%202025-04-24%20013739.png" width="800" alt="Sample 6"/>
  <img src="images/Screenshot%202025-04-24%20013750.png" width="800" alt="Sample 7"/>
</p>
