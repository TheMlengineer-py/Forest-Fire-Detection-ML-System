Forest Fire Detection System
Overview
This project involves developing a Support Vector Machine (SVM) model to detect forest fires based on the Algeria forest fire dataset. The model was trained using four features: Temperature, Relative Humidity, Windspeed, and Rainfall.
•	Training Accuracy: 93%
•	Wall-time: 2ms
•	Overall Mean Accuracy: 91.8%
•	Standard Deviation: 0.0745
Deployment
The deployment lifecycle of the machine learning model includes saving the model using the Python pickle library and deploying it into production on Heroku using the Flask micro-web framework. The code pipeline connects the GitHub repository, which holds the development files, to the Heroku production infrastructure.
Key Points
•	Hosting: The application is hosted on Heroku's free dynos, which sleep after 30 minutes of inactivity to save hosting hours.
•	Application Slug Size: 142.1MiB of the 500MiB limit.
•	Buildpacks: Python/Heroku.
Directory Structure
The main directory of the application consists of the following files:
1.	Templates Folder
o	Contains index.html, which serves as the frontend of the application. It is built using Bootstrap, CSS, and HTML.
2.	. gitignore
o	Lists files and directories to be ignored by Git during the production process.
3.	dataset.csv
o	Contains the Algerian forest fire dataset.
4.	app.py
o	Contains the Flask application, the loaded model from the pickle library, and backend code. This is the root of the application.
5.	Jupyter Notebook
o	Includes Exploratory Data Analysis (EDA), cleaned and balanced datasets, visualizations, trained models, and the saved model.
6.	model.pkl
o	Holds the serialized model, enabling objects to be saved to disk and loaded back into the program at runtime.
7.	Procfile
o	Specifies the commands to be executed by the application at startup, defining the web process type during production.
8.	requirements.txt
o	Lists all dependencies required for the web-based application development.
9.	runtime.txt
o	Specifies the Python version used for application development.
Getting Started
Prerequisites
•	Python 3.x
•	Flask
•	Heroku CLI
•	Git
Installation
1.	Clone the repository:
bash
Copy code
git clone https://github.com/your-username/forest-fire-detection.git
2.	Navigate to the project directory:
bash
Copy code
cd forest-fire-detection
3.	Install dependencies:
bash
Copy code
pip install -r requirements.txt
Running the Application
1.	Run the Flask application:
bash
Copy code
python app.py
2.	Access the application: Open your browser and navigate to http://127.0.0.1:5000/.
Deploying to Heroku
1.	Login to Heroku:
bash
Copy code
heroku login
2.	Create a new Heroku app:
bash
Copy code
heroku create your-app-name
3.	Push the code to Heroku:
bash
Copy code
git push heroku main
4.	Open the Heroku app:
bash
Copy code
heroku open
Contributions
Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your code adheres to the existing coding standards and include relevant tests.
License
This project is licensed under the MIT License. See the LICENSE file for more details.
________________________________________
For any questions or support, please open an issue in the repository or contact me directly at dayo.dataengineer@gmail.com.


link to the web-based application
https://flask--prediction.herokuapp.com/
