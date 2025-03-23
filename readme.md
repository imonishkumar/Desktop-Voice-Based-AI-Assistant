# Desktop Voice Based AI Assistant

An AI-powered desktop assistant built with Python that includes voice recognition, face authentication, and automation features.

---

## 📌 Project Setup Instructions
Follow these steps to set up the project on your system.

### **➕ 1. Clone the Project**
```bash
git clone https://github.com/your-repo/desktop-assistant.git
cd desktop-assistant
```

### **➕ 2. Create a Virtual Environment**
```bash
python -m venv venv
```

### **➕ 3. Activate the Virtual Environment**
#### Windows:
```bash
venv\Scripts\activate
```
#### Mac/Linux:
```bash
source venv/bin/activate
```

### **➕ 4. Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## 🔧 Update File Locations
Some file paths in the project need to be updated based on your system.

### **➕ Update `engine/features.py`**
#### **Old Path:**
```python
music_dir = "c:\\cook\\Final Project\\desktop assistant\\www\\assets\\audio\\start_sound.mp3"
```
#### **New Path:**
```python
music_dir = "C:\\Users\\YourUsername\\Desktop\\assistant\\www\\assets\\audio\\start_sound.mp3"
```

### **➕ Update `engine/auth/recoganize.py`**
#### **Old Path:**
```python
recognizer.read('C:\\cook\\Final Project\\desktop assistant\\engine\\auth\\trainer\\trainer.yml')
cascadePath = "C:\\cook\\Final Project\\desktop assistant\\engine\\auth\\haarcascade_frontalface_default.xml"
```
#### **New Path:**
```python
recognizer.read('C:\\Users\\YourUsername\\Desktop\\assistant\\engine\\auth\\trainer\\trainer.yml')
cascadePath = "C:\\Users\\YourUsername\\Desktop\\assistant\\engine\\auth\\haarcascade_frontalface_default.xml"
```

### **➕ Update `engine/auth/sample.py`**
#### **Old Path:**
```python
detector = cv2.CascadeClassifier('C:\\cook\\Final Project\\desktop assistant\\engine\\auth\\haarcascade_frontalface_default.xml')
cv2.imwrite('C:\\cook\\Final Project\\desktop assistant\\engine\\auth\\samples\\face.' + str(face_id) + '.' + str(count) + ".jpg", converted_image[y:y+h,x:x+w])
```
#### **New Path:**
```python
detector = cv2.CascadeClassifier('C:\\Users\\YourUsername\\Desktop\\assistant\\engine\\auth\\haarcascade_frontalface_default.xml')
cv2.imwrite('C:\\Users\\YourUsername\\Desktop\\assistant\\engine\\auth\\samples\\face.' + str(face_id) + '.' + str(count) + ".jpg", converted_image[y:y+h,x:x+w])
```

---

## 🔐 Setup Hugging Face Authentication
The assistant uses `hugchat` for AI features, which requires authentication.

### **➕ 1. Create `cookies.json`**
- Generate a **Hugging Face token** from [Hugging Face](https://huggingface.co/settings/tokens).
- Create a `cookies.json` file inside your project directory.

### **➕ 2. Add the Following Content to `cookies.json`**
```json
{
    "your_domain": "ai.yourdomain.huggingface.co",
    "token": "your_huggingface_api_token"
}
```
- Replace **`"your_domain"`** with your Hugging Face domain.
- Replace **`"your_huggingface_api_token"`** with your API token.

---

## 🚀 Run the Assistant
Once everything is set up, start the assistant:
```bash
python run.py
```
Enjoy your AI-powered **Desktop Assistant!** 🎧💻

---

## 🛠️ Troubleshooting
### **🛠️ Missing Module?**
Reinstall dependencies:
```bash
pip install -r requirements.txt
```
### **🛠️ Voice Recognition Not Working?**
Manually install `pyaudio`:
```bash
pip install pyaudio
```

---

## 📃 License
This project is licensed under **MIT License**.

