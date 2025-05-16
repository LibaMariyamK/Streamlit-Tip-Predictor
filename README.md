# Machine Learning Model Deployment using Streamlit
[Tip Prediction APP](https://m7j8rqqsfatqy3zrv7apuu.streamlit.app/)

### **Project Overview**

The project consists of two main parts:

1. **Model Training** (using a dataset like `tips` from Seaborn and RandomForestRegressor for prediction).
2. **Web Application** using Streamlit for taking user inputs and displaying predictions.

###  **Model Training and Saving** (`model.py`)

#### **Training the Model**

1. We load the dataset using Seaborn's built-in `load_dataset('tips')`.
2. We manually encode categorical variables like `sex`, `smoker`, `day`, and `time`.
3. We use **RandomForestRegressor** to predict the tip based on the features.
4. After training the model, we save it using `pickle`.

### **Streamlit App** (`app.py`)

#### **Creating the Streamlit Web Interface**

1. We load the trained model (`model.pkl`).
2. The app allows users to input data (like `total_bill`, `size`, `sex`, etc.) using Streamlit widgets.
3. Once the user provides inputs and clicks the **"Predict Tip"** button, the model predicts the tip and displays it.

### **Running Locally**

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
