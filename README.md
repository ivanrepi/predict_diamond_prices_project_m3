# Diamond Price Predictor

In this project, a Supervised Machine Learning algorithm has been built, which will allow us to predict the price of a Diamond.

![Image](https://www.genesisdiamonds.net//media/wysiwyg/DIAMOND-BUYING-PAGE-banner.jpg)

---
## **Description**
Given a certain features of a Diamond, the model will predict the sales price of that one.

To better Diamonds understanding as well as data cleaning process, check my [previous project](https://github.com/ivanrepi/data_visualization_project_m2) !

&nbsp;
## **Diamonds Dataset** :

The price of a diamond has a direct correlation with its carat. It is not a straight linear correlation but an exponential one. There are other relevant features which also influence its price, such as color, clarity and cut.

<p align="center"><img src="https://i.imgflip.com/3l8sg9.jpg"></p>


This classic dataset contains the prices and other attributes of almost 44,000 diamonds. It's a great dataset for machine learning and work with data analysis and visualization.

Dataset Columns :
- **price** : price in US dollars ( $326 - $18,823 )

- **carat** : weight of the diamond ( 0.2 - 5.01 )

- **cut** : quality of the cut ( Fair , Good , Very Good , Premium , Ideal )

- **color** : diamond colour, from J ( worst ) to D ( best )

- **clarity** : a measurement of how clear the diamond is ( I1 (worst) ,SI2 ,SI1 ,VS2 ,VS1 ,VVS2 ,VVS1 ,IF (best))

- **x** : length in mm ( 0 - 10.74 )

- **y** : width in mm ( 0 - 58.9 )

- **z** : depth in mm ( 0 - 31.8 )

- **depth** : total depth percentage = z / mean( x, y ) = 2 * z / ( x + y ) --> ( 43 - 79 )

- **table** : width of top of diamond relative to widest point ( 43 - 95 )

![Image](https://4cs.gia.edu/wp-content/uploads/2016/08/PUBL160028_SC_4Cs_Spokes_990x500_ENG_v1.jpg)


---
## **Getting Started**
### :baby: **Status**
This is part of Kaggle Competition. The main goal is to build a complete ML model.

### :computer: **Dependencies**

- This repository is tested on **Python 3.7+**.
- Create a virtual environment with the version of Python you're going to use and activate it.

- Install [pandas](https://pandas.pydata.org/docs/user_guide/index.html) library. Copy and paste next command in your master branch:
    ```
    conda install pandas
    ```
- Install [scikit-learn](https://scikit-learn.org/stable/) library. Copy and paste next command in your master branch:
    ```
    pip install -U scikit-learn
    ```
- Install [XGBoost](https://xgboost.readthedocs.io/en/stable/) library. Copy and paste next command in your master branch:
    ```
    pip install xgboost
    ```
- Install [matplotlib](https://matplotlib.org/stable/index.html) library. Copy and paste next command in your master branch:
    ```
    pip install matplotlib
    ```
- Install [seaborn](https://seaborn.pydata.org/) library. Copy and paste next command in your master branch:
    ```
    pip install seaborn
    ```



&nbsp;

---
## :lock: **ADMIN ROLE**

### :clipboard: **Overview**
Admin role should chose what kind of 'Place of Interest' the user will use. It can be obtained [here](https://datos.madrid.es/nuevoMadrid/swagger-ui-master-2.2.10/dist/index.html?url=/egobfiles/api.datos.madrid.es.json#/).

The app includes a double authentication step. Admin will receive a security number in his/her email, to verify his/her identity.


### :wrench: **Installing**
Once all dependencies are clear, follow the next steps to install it:
1. Clone this [repo](https://github.com/ivanrepi/nearest_bicimad_station)
2. Create an account on EMT Madrid developer website ([here](https://mobilitylabs.emtmadrid.es/es/doc/new-app))
3. In your local repository, create the file ".env", with the next parameters:
    ```
    path="path of the repo"

    sender_email = "type your email" 
    password_sender = "type your email password"
    admin_email="type admin email" #For double auth. Can be different of the sender one
    emt_madrid_email="email from step 2"
    emt_madrid_pwd="password from step 2"
    ```
4. Open the main_admin.py file, and edit the URL of the 'Place of Interest'. By default, it is settled "Instalaciones Deportivas Básicas de Madrid".

### :point_right: **Executing program**
1. Open the terminal.
2. Look for the main_admin.py file in your repo.
3. Execute the next command:
    ```
    python main_admin.py
    ```
4. It will ask you for an admin email. It should be the same settled in ".env" file.
5. If email address is correct, admin should receive a security code in his/her email.
6. Type this code in the terminal and press enter.
7. If code is correct, it starts the process to prepare the result table (which one that user will work with).

### :boom: **Core technical concepts and inspiration**
The main goal of this role is to work with double authentication mode, as well as divide the app in two kind of users. 
Working with this division, final user will not have to wait for data preparation (as this is part of the admin work)

&nbsp;



---

### :file_folder: **Folder structure**
```
└── project
    ├── __trash__
    │ 
    ├── .git
    │ 
    ├── .gitignore
    │ 
    ├── nearest_bicimad_station.html
    │ 
    ├── README.md
    │ 
    ├── main_user.py
    │ 
    ├── main_admin.py
    │ 
    ├── modules
    │   └── geo_calculations.py
    │ 
    ├── p_acquisition
    │   └── acquisition.py
    │
    ├── p_wrangling
    │   └── wrangling.py
    │
    ├── p_analysis
    │   └── analysis.py
    │
    ├── p_reporting
    │   └── reporting.py
    │
    └── data
        ├── raw
        ├── processed
        └── results
```

> Do not forget to include `__trash__` and `.env` in `.gitignore` 

&nbsp;
### :shit: **ToDo**
:black_square_button: Create an API to connect to Places of Interests webstite.  
:black_square_button: Get all places of interest at the same time, and not have to settled it in the main_admin script.  
:black_square_button: Add possibility to go by car, walking or taxi to the nearest BiciMad station.  
:black_square_button: Create the UI to help the final user to use it.  

---


