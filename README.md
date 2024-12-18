# **Sepsis Prediction System**  

---

## **Overview**  
The **Sepsis Prediction System** is a machine learning-powered web application developed by **Benjamin Agbleke** as part of his final project for Azubi Africa. This innovative tool predicts the likelihood of sepsis in patients using clinical data, offering healthcare providers actionable insights to enable early intervention and improve patient outcomes.  

The application includes:  
- A machine learning model trained on clinical data.  
- A REST API built using **FastAPI** for making predictions.  
- A containerized deployment with **Docker** for scalability and reliability.  
- A user-friendly interface hosted online for seamless access.  

---

## **Table of Contents**  
1. [Overview](#overview)  
2. [Setup](#setup)  
   - [Prerequisites](#prerequisites)  
   - [Installation Steps](#installation-steps)  
3. [Usage](#usage)  
   - [API Endpoints](#api-endpoints)  
4. [Dataset Description](#dataset-description)  
   - [Features Overview](#features-overview)  
   - [Target Column](#target-column)  
5. [Model Development](#model-development)  
   - [Data Preprocessing](#data-preprocessing)  
   - [Model Training and Evaluation](#model-training-and-evaluation)  
6. [Future Enhancements](#future-enhancements)  
7. [Deployed Application](#deployed-application)  
8. [Author](#author)  
9. [License](#license)  

---

## **Setup**  

### **Prerequisites**  
To set up and run this project, ensure you have the following installed:  
1. **Python**: Version 3.8 or later.  
2. **Docker**: Installed and running on your machine.  
3. **Git**: To clone the project repository.  
4. **Web Browser**: For accessing the deployed application.  

### **Installation Steps**  
Follow these steps to install and set up the project:  

1. **Clone the Repository**  
   Clone the project to your local system using Git:  
   ```bash  
   git clone <repository_url>  
   cd <repository_directory>  
   ```  

2. **Install Dependencies**  
   Install all required Python libraries:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. **Build the Docker Image**  
   Create a Docker image for the application:  
   ```bash  
   docker build -t sepsis-prediction .  
   ```  

4. **Run the Docker Container**  
   Start the application using Docker and expose it on port 8000:  
   ```bash  
   docker run -p 8000:8000 sepsis-prediction  
   ```  

5. **Access the Application**  
   Open your browser and navigate to:  

   ```http  
   http://localhost:8000  
   ```  

---

## **Usage**  

### **API Endpoints**  
The application provides a REST API for predictions:  

- **POST /predict**  
  **Description**: Accepts patient data in CSV format and returns a sepsis prediction.  
  **Response Example**:  
  ```json  
  {  
      "prediction": 0  
  }  
  {  
      "prediction": 1  
  }  
  ```  

---

## **Dataset Description**  

### **Features Overview**  
The dataset includes the following clinical features:  

| **Feature**      | **Description**                              | **Data Type** |  
|-------------------|----------------------------------------------|---------------|  
| **PRG**           | Plasma glucose concentration                 | Integer       |  
| **PL**            | Blood pressure level                         | Integer       |  
| **PR**            | Pulse rate                                   | Integer       |  
| **SK**            | Skin thickness                               | Integer       |  
| **TS**            | Time since the last medical test             | Integer       |  
| **M11**           | Medical measurement 11                      | Float         |  
| **BD2**           | Blood density metric 2                      | Float         |  
| **Age**           | Age of the patient                          | Integer       |  
| **Insurance**     | Insurance status (0: Uninsured, 1: Insured) | Integer       |  

### **Target Column**  
- **Sepsis**: Indicates whether sepsis is present:  
  - **Positive**: Patient likely has sepsis.  
  - **Negative**: Patient likely does not have sepsis.  

---

## **Model Development**  

### **Data Preprocessing**  
The following steps were performed to prepare the dataset for model training:  
- **Handling Missing Values**: Imputed missing values using statistical techniques to ensure data completeness.  
- **Feature Standardization**: Standardized features to maintain consistent scaling across variables.  
- **Train-Test Split**: Split the dataset into training (80%) and testing (20%) subsets to evaluate model performance effectively.  

### **Model Training and Evaluation**  
- Various machine learning models were tested, including:  
  - **Logistic Regression**  
  - **Random Forest**  
  - **Gradient Boosting**  
- **Evaluation Metrics**:  
  - Accuracy  
  - Precision  
  - Recall  
  - F1 Score  

The final model demonstrated high accuracy on the test dataset and robust generalization on unseen data, making it suitable for deployment.  

---

## **Future Enhancements**  

1. **Model Optimization**: Apply advanced techniques like hyperparameter tuning and ensemble methods to enhance model performance.  
2. **Real-Time Predictions**: Implement streaming data inputs to enable real-time sepsis prediction for live monitoring.  
3. **User Dashboards**: Develop interactive graphical dashboards using tools like **Streamlit** or **Plotly Dash** to visualize prediction trends and insights.  
4. **Mobile Integration**: Create a mobile application for healthcare providers to access predictions on the go.  
5. **EHR Integration**: Seamlessly integrate with Electronic Health Record (EHR) systems to enhance hospital workflows and patient data analysis.  

---

  

---

## **Author**  
**Benjamin Agbleke**  
Benjamin is a  **Data Analyst** currently pursuing studies in Data Analysis. He possesses strong skills in data preprocessing, model building, and visualization. This project, the **Sepsis Prediction System**, represents his **Final Project Work 3** for Azubi Africa, showcasing his ability to apply data analytics and machine learning in solving real-world problems.  

---


