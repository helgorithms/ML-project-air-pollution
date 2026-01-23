
# Machine Learning Project - Urban Air Pollution

**Project**  

The "Urban Air Pollution Challenge" is a public data science challenge which can be found on [Zindi](https://zindi.africa/competitions/zindiweekendz-learning-urban-air-pollution-challenge/leaderboard). The objective is to predict air quality in various locations around the globe using weather and satellite data. 

**Framework**

This project was part of the data science bootcamp at SPICED/NeueFische Academy in Berlin/ Germany. The project was a solo project.

## Folder Structure
- `data` contains the data set `Train.csv`
- `images` contains all plots
- `presentation` contains the project presentation

## File Structure
- `ML-project.ipynb` contains the main project notebook
- `Missing-values.ipynb`contains the visualization of all missing values pre-cleaning
- `requirements.txt`contains all required software versions for this project
- `Makefile` contains the installation configuration for the virtual environment (see below for instructions)
-`LICENSE`contains the MIT software license



## Set up your Environment


### **`macOS`** type the following commands : 

- For installing the virtual environment you can either use the [Makefile](Makefile) and run `make setup` or install it manually with the following commands:

     ```BASH
    make setup
    ```
    After that active your environment by following commands:
    ```BASH
    source .venv/bin/activate
    ```
Or ....
- Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
    
### **`WindowsOS`** type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-bash` CLI :
  
    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:
    ```Bash
    python.exe -m pip install --upgrade pip
    ```


   
## Usage

In order to train the model and store test data in the data folder and the model in models run:

**`Note`**: Make sure your environment is activated.

```bash
python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.


---

## Handling Merge Conflicts in Jupyter Notebooks

When working in teams, `.ipynb` files can cause messy merge conflicts because they’re JSON-based.  
We use **nbdime** to make this easy.

### Setup (run once)
```bash
nbdime config-git --enable
```

### When a conflict happens
```bash
nbdime mergetool
```

A web interface will open showing both notebook versions side by side.
Choose what to keep, save and close tool, then:
```bash
git add your_notebook.ipynb
git commit -m "Resolved notebook conflict"
```
That’s it — clean merges for notebooks!