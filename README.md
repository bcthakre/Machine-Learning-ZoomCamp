# Machine-Learning-ZoomCamp

# Week2

# How to create new conda enviornment

conda create -n <name_enviornment> python=3.9

# How to use newly create conda enviornment

conda activate <name_enviornment>

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