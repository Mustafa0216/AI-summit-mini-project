Used Car Price Predictor (Streamlit App)
This project implements a web application using Streamlit to predict the resale value of used cars. It utilizes various machine learning models such as Random Forest, XGBoost, and Gradient Boosting to make predictions based on car features.

Features
Interactive UI: Built with Streamlit for an intuitive user experience.
Multiple Models: Choose between Random Forest, XGBoost, and Gradient Boosting Regressors.
Real-time Prediction: Get instant car price predictions based on user input.
Model Evaluation: Displays RMSE and R² scores for the selected model.
Setup and Installation
To run this project, you'll need Python and the following libraries. It's recommended to use a virtual environment.

Clone the repository (or download the files):

# Assuming you have the notebook content as files
Install the required Python packages:

!pip install streamlit pandas scikit-learn xgboost
Ensure you have the data file: Make sure car data.csv is in the same directory as your app.py.

How to Run the App
Save the Streamlit application code: The Streamlit application code is in the app.py file. If you haven't already, save the provided app.py content into a file named app.py.

Run the Streamlit app: In your terminal (or Colab cell), navigate to the directory where app.py is saved and run:

!streamlit run app.py
If running in Google Colab, you might use a tunneling service like localtunnel or ngrok to expose the app:

import urllib
print("Password/Enpoint IP for localtunnel is:", urllib.request.urlopen('https://ipv4.icanhazip.com').read().decode('utf8').strip("\n"))

!streamlit run app.py & npx localtunnel --port 8501

#Or with ngrok:

from pyngrok import ngrok
ngrok.set_auth_token("YOUR_NGROK_AUTH_TOKEN") # Replace with your actual ngrok auth token
ngrok.kill()
tunnel = ngrok.connect(8501)
print(f" Click this link to open your app: {tunnel.public_url}")
!streamlit run app.py >/dev/null
Usage
Once the Streamlit app is running:

Model Selection: Use the sidebar to choose between "Random Forest", "XGBoost", or "Gradient Boosting" models.
Model Performance: The sidebar will display the RMSE and R² score for the selected model on the test data.
Input Car Details: Enter the car's age, fuel type, transmission, owner number, and kilometers driven.
Get Prediction: Click the "Predict" button to see the estimated resale value of the car.
