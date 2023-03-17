# Machine-Learning-ZoomCamp

# Week2

# How to create new conda enviornment

conda create -n <name_enviornment> python=3.9

# How to use newly create conda enviornment

conda activate <name_enviornment>

# How to see the conda enviornment

conda env list

# how to install multiple packages through pip

a. create requirements.txt
b. add all the packages in separate line
c. Run the following command
1. pip install -r requirements.txt

# how to check the installed package

pip list

# how to run mlflow with backend of sqlite

mlflow ui --backend-store-uri sqlite:///mlflow.db

# The artifacts will be generated in the new folder as jupyter notebook 
# the mlruns folder will be created automatically when following command is run

mlflow.set_tracking_uri('sqlite:///mlflow.db')

# If getting the following error
[2023-03-17 22:42:15 +0000] [17595] [ERROR] Can't connect to ('127.0.0.1', 5000)
Running the mlflow server failed. Please see the logs above for details.

do the following

1. lsof -i :5000
2. kill -9 <pid_running>