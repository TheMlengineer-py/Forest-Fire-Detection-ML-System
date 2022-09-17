# flask-deploy
Forest Fire Detection 

The machine learning model was trained on the Algeria forest fire dataset collected over two regions in Algeria.

SUPPORT VECTOR MACHINE DEPLOYMENT
The machine learning model deployment life cycle was explained in this section. The model was saved by dumping support vector machine in the python pickle library, support vector machine was deployed into production(Heroku cloud computing infrastructure server) using Flask micro-web framework by creating a code pipeline which connects GitHub repository holding the development files with the Heroku production infrastructure where the application is hosted remotely on the free dynos which serves as a container for the web-based application and performs real time prediction for up to 1000hours monthly, when the dynos does not receive a web request in a 30-minute period, it sleeps to save up hosting hours. Application slug size of 142.1MiB of 500MiB and Python/Heroku as the buildpacks
The application main directory consists of the following files.
i. Templates folder which holds file named index.html which serves as frontend of the application made up of boostrap, css and html codes. Basically, it serves as the homepage of the application.
ii. gitiignore file holds an extensive list of untracked files which are to be ignored during the production process by Git
iii. The csv file holds the Algerian forest fire dataset.
iv. app.py file holds the flask application, loaded model from the pickle library and backend codes, it is the application root.
v. Jupiter notebook file holds the Exploratory Data analysis, Cleaned and balanced dataset, visualization, trained models, and the saved model.
vi. model.pkl file holds the dumped model, which enables objects to be serialized to files on disk and deserialized back into the program at runtime.
vii. Procfile which provides the web process type during the production, it specifies the commands that are executed by the application on the startup.
viii. requirements.txt file listing all the dependencies for the web-based application development.
ix. Runtime.txt contains the python version for the application development.
All the files listed were pushed to GitHub repository from which a code pipeline connecting the development files to the Heroku cloud server was created.
