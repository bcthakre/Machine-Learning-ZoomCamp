# Machine-Learning-ZoomCamp

# Week2

## How to create new conda enviornment

```
conda create -n <name_enviornment> python=3.9
```

## How to use newly create conda enviornment
```
conda activate <name_enviornment>
```
## How to see the conda enviornment
```
conda env list
```
## how to install multiple packages through pip

a. create requirements.txt
b. add all the packages in separate line
c. Run the following command
```
pip install -r requirements.txt
```
## how to check the installed package
```
pip list
```
## how to run mlflow with backend of sqlite
```
mlflow ui --backend-store-uri sqlite:///mlflow.db
```
## To run mlflow on other port 

mlflow ui --backend-store-uri sqlite:///mlflow.db --port 8000

```
## The artifacts will be generated in the new folder as jupyter notebook 
## the mlruns folder will be created automatically when following command is run
```
mlflow.set_tracking_uri('sqlite:///mlflow.db')
```
## If getting the following error

<pre>
```plaintext
[2023-03-17 22:42:15 +0000] [17595] [ERROR] Can't connect to ('127.0.0.1', 5000) Running the mlflow server failed. Please see the logs above for details.
```
</pre>

do the following
```
lsof -i :5000
kill -9 <pid_running>
you can also kill multiple process open in a particular port with the following command

lsof -i :5000 | awk 'NR>1 {print $2}' | xargs kill


```

```
## Following commands have changed 

list_registered_models ==> search_registered_models
list_experiments ==> search_experiments
```