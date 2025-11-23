# 🔬 AI Blood Group Analyzer Using Fingerprint
![Demo Video](images/BloodGroup.gif)

An AI-powered web application that detects blood groups (A+, A-, B+, B-, AB+, AB-, O+, O-) from fingerprint images using deep learning. Built with PyTorch and Flask, this project provides a complete user authentication system and intuitive web interface for blood group prediction.

---

## 🚀 Key Features

- 🧠 **Custom CNN Model**: SimpleCNN architecture with 2 convolutional layers trained on fingerprint dataset
- 🔐 **User Authentication**: Complete signup/login system with password hashing using SQLite database
- 🌐 **Web Interface**: Modern, responsive Flask web application with multiple pages
- 📊 **Blood Group Classification**: Supports all 8 blood types (A+, A-, B+, B-, AB+, AB-, O+, O-)
- 🖼️ **Image Upload**: Easy-to-use interface for uploading fingerprint images
- ⚡ **Real-time Prediction**: Instant blood group detection using trained PyTorch model

---

## 🔍 Technologies & Stack

**Backend:**
- Python 3.x
- Flask (Web Framework)
- PyTorch (Deep Learning)
- SQLite (Database)
- Werkzeug Security (Password Hashing)

**Frontend:**
- HTML/CSS/JavaScript
- Bootstrap 5
- Bootstrap Icons
- AOS (Animate On Scroll)
- GLightbox
- Swiper
- Typed.js

**Machine Learning:**
- PyTorch
- torchvision
- PIL (Image Processing)
- Custom SimpleCNN Architecture

---

## 📁 Project Structure

```
Blood/
├── Code/
│   ├── app.py                      # Main Flask application
│   ├── Model.pth                   # Trained PyTorch model
│   ├── Training_Code.ipynb         # Model training notebook
│   ├── dataset_blood_group/        # Training dataset (8 classes)
│   │   ├── A+/
│   │   ├── A-/
│   │   ├── AB+/
│   │   ├── AB-/
│   │   ├── B+/
│   │   ├── B-/
│   │   ├── O+/
│   │   └── O-/
│   ├── templates/                  # HTML templates
│   │   ├── hospitalhomepage.html
│   │   ├── login.html
│   │   ├── signup.html
│   │   ├── login2.html            # Prediction page
│   │   ├── result.html
│   │   ├── about.html
│   │   ├── chart.html
│   │   └── team.html
│   ├── static/                     # Static assets
│   │   ├── css/
│   │   ├── js/
│   │   ├── uploads/               # User uploaded images
│   │   └── vendor/                # Third-party libraries
│   └── Test Images/               # Sample test images
├── images/                         # Demo screenshots
└── README.md
```

---

## 🚀 Installation & Setup

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Step-by-Step Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/CodewithShaaz/AI-Bloodgroup-Analyzer-using-fingerprint.git
   cd AI-Bloodgroup-Analyzer-using-fingerprint
   ```

2. **Install required dependencies:**
   ```bash
   pip install flask torch torchvision pillow flask-wtf wtforms
   ```

3. **Navigate to the Code directory:**
   ```bash
   cd Code
   ```

4. **Ensure Model.pth exists:**
   - The trained model (`Model.pth`) should be present in the `Code/` directory
   - If missing, you'll need to train the model using `Training_Code.ipynb`

5. **Run the Flask application:**
   ```bash
   python app.py
   ```

6. **Access the application:**
   - Open your browser and navigate to: `http://127.0.0.1:5000`
   - The database (`users.db`) will be created automatically on first run

---

## 💡 How to Use

1. **Homepage**: Visit the landing page at `http://127.0.0.1:5000`
2. **Sign Up**: Create a new account with your details
3. **Login**: Access your account using credentials
4. **Upload Image**: Navigate to the prediction page and upload a fingerprint image
5. **Get Results**: View the predicted blood group instantly

---

## 🧠 Model Architecture

**SimpleCNN Details:**
- **Input**: 224×224 RGB fingerprint images
- **Conv Layer 1**: 3→32 channels, 3×3 kernel
- **Conv Layer 2**: 32→64 channels, 3×3 kernel
- **Pooling**: MaxPool2d (2×2)
- **FC Layer 1**: 64×56×56 → 512
- **FC Layer 2**: 512 → 8 (output classes)
- **Optimizer**: SGD with momentum (0.9), learning rate 0.001
- **Loss Function**: CrossEntropyLoss
- **Training**: 25 epochs with 80/20 train-validation split

---

## 📊 Dataset

The model was trained on a fingerprint dataset organized into 8 classes:
- **A+, A-, B+, B-, AB+, AB-, O+, O-**
- Images preprocessed to 224×224 resolution
- Normalized using ImageNet statistics
- Data split: 80% training, 20% validation

---

## 🔒 Security Features

- Password hashing using `pbkdf2:sha256`
- Session-based authentication
- Protected routes requiring login
- Secure database operations with SQLite
- Flash messages for user feedback

---

## 🌐 Application Routes

| Route | Method | Description |
|-------|--------|-------------|
| `/` | GET | Homepage |
| `/signup` | GET, POST | User registration |
| `/login` | GET, POST | User authentication |
| `/logout` | GET | End user session |
| `/predict_blood_group` | GET | Upload page (protected) |
| `/predict` | POST | Process image & predict |
| `/about` | GET | About page |
| `/chart` | GET | Charts page |
| `/team` | GET | Team page |

---

## 📌 Future Enhancements

- Improve model accuracy with larger, diverse datasets
- Add result history and user dashboard
- Implement REST API for mobile integration
- Deploy to cloud platforms (AWS, Azure, Heroku)
- Add real-time camera capture for fingerprint scanning
- Multi-language support
- Export results as PDF

---

## 👨‍💻 Author

**CodewithShaaz**
- GitHub: [@CodewithShaaz](https://github.com/CodewithShaaz)

---

## 📄 License

This project is open source and available for educational purposes.
