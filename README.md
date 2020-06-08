
# 1. Project Title:
## Using PySpark for Recipe Classification on basis of Ingredients and Cooking Time.

# 2. Description
To use PySpark to Filter recipes with beef as a ingredient and calculate the average cooking time then Classify with its difficulty levels (cooking time).


**formula**
**total_cook_time = cookTime + prepTime**

**Criteria** | **total_cook_time**
------------ | -------------
easy | less than 30 mins
medium | between 30 and 60 mins
hard | more than 60 mins.



## 2.1 About the Dataset
This is a dataset with a collection of various cooking recipes, with these attributes - name, ingredients, url, image, cookTime, recipeYield, datePublished, prepTime, description.

## 2.2 Code Outline
**High-level Overview**
    - Load Data
    - Transform Data
    - Filter data
    - Difficulty metrics

- - - -

# 3. Special Instructions
Default ```base_dir``` for dataset is ```deepsat-sat6```. Hence, try keeping the notebook and this directory in the same folder. It also the notebook assumes by default that data generated from AWS is stored under  ```fromAWS``` folder. For ease of use, data generated from our experiments from AWS is provided in that directory.

Since, the actual dataset is a space consuming ```(~5.6 GB)```, we have only provided a small set of that dataset, original dataset can be downloaded from the above link of Kaggle which only has ```first 200 rows``` with filenames having suffix ```_200```.

Following file structure is advised: (in case of errors, please consult this)
```
./
... HelloFresh.py
... Readme.md
... requirements.txt
... test_isoTimeToMin.py
... UtilsETL.py
... input/
... ... recipes.json
... output/
... ... report.csv

```

**Note**
- Here, filename ```pca_200.model``` could be different, based on the number of pca components chosen, here it is ```k=200```.

- For running ```project_deepsat_aws.py```,  more information can be found inside the file.  If you want test the find, you can supply option ```--demo```, which will only take rows 5 rows. This behaviour can be changed in the code by supplying different values.

```
#To run locally
python HelloFresh.py --inputPath ./WorkTest/input/recipes.json --outputPath ./WorkTest/output/report.csv --filterColumn ingredients --filterValue beef


```

- - - -

# 4. Additional Libraries
You can install necessary packages to run these codes by running the following:
```pip install -r requirements.txt```

- - - -

# 5. Known Issues
Loading entire dataset on local machine causes```Java Heap Memory ``` issues, hence use small toy dataset with suffix ```_200``` or consult the notebook for more details.
- - - -
