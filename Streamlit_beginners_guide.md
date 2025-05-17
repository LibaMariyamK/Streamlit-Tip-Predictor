## 🌟 Streamlit

### 📌 What is Streamlit?

**Streamlit** is an open-source Python library that helps you turn data scripts into interactive web apps in just a few lines of code. It's popular among data scientists and ML engineers.

### ✅ Key Features

* No need for front-end knowledge (HTML/CSS/JS)
* Supports widgets like sliders, buttons, text input
* Real-time updates with minimal code
* Works great with Pandas, Matplotlib, Plotly, etc.

---

## 🚀 Getting Started

### 🛠️ Installation

```bash
pip install streamlit
```

### 🔄 Run Your First App

Create a file `app.py` and write:

```python
import streamlit as st

st.title("Hello, Streamlit!")
st.write("This is your first Streamlit app 🎉")
```

Now run it:

```bash
streamlit run app.py
```

---

## 📂 Basic Components

### 🎯 Display Elements

```python
st.title("Main Title")
st.header("Header Text")
st.subheader("Subheader Text")
st.text("Plain text")
```

### 📝 Input Widgets

```python
name = st.text_input("Enter your name:")
age = st.number_input("Enter your age:", min_value=0, max_value=100)
agree = st.checkbox("I agree")
sex = st.selectbox("Sex", ["Male", "Female"])
```

### 📈 Display Data

```python
import pandas as pd

df = pd.DataFrame({
    'Name': ['Alice', 'Bob'],
    'Age': [24, 27]
})
st.dataframe(df)
```

### 📊 Charts

```python
import numpy as np
import matplotlib.pyplot as plt

data = np.random.randn(100)
st.line_chart(data)
st.area_chart(data)
st.bar_chart(data)
```

### 🖼️ Display Media

```python
st.image("image.jpg", caption="Sample Image")
st.video("https://www.youtube.com/watch?v=abcd1234")
```

---

## 🔄 Buttons and Interactions

```python
if st.button("Click Me"):
    st.write("You clicked the button!")
```

---


## 📚 Example Mini App

```python
import streamlit as st
import pandas as pd

st.title("Simple BMI Calculator")

height = st.number_input("Enter your height (in cm):")
weight = st.number_input("Enter your weight (in kg):")

if st.button("Calculate BMI"):
    bmi = weight / ((height / 100) ** 2)
    st.write(f"Your BMI is: {bmi:.2f}")
```

---


#### **Running Locally**

1. Install Streamlit:

   ```bash
   pip install streamlit
   ```
2. Run the app locally by executing:

   ```bash
   streamlit run app.py
   ```
3. This will launch the Streamlit interface in your browser where you can interact with the app.

### **Deploying to Streamlit Cloud via GitHub**

To deploy your app on **Streamlit Cloud** using GitHub, follow these steps:

#### **Step 1: Set Up GitHub Repository**

1. Create a GitHub repository and push your project files (including `app.py`, `requirements.txt`, etc).
2. **`requirements.txt`** should include the necessary libraries,
    to create one:

   ```bash
   pip freeze > requirements.txt
   ```

#### **Step 2: Deploy on Streamlit Cloud**

1. Go to [Streamlit Cloud](https://streamlit.io/sharing).
2. Sign in to Streamlit Community Cloud with Your Github
3. Click on "Create App"
4. Link your GitHub repository.
5. Select the correct branch and file (`app.py`), then click **Deploy**.
6. The app will be deployed, and you’ll receive a live URL to access it.

#### **Step 3: Automate Deployment (Optional)**

To ensure your Streamlit app updates automatically:

* Push changes to GitHub, and Streamlit Cloud will automatically redeploy.

