
# ETL using PySpark

## 1.Description
To use PySpark to Filter recipes with beef as a ingredient and calculate the average cooking time then Classify with its difficulty levels (cooking time).


**Formula :** ```total_cook_time = cookTime + prepTime```

**Criteria** | **total_cook_time**
------------ | -------------
easy | less than 30 mins
medium | between 30 and 60 mins
hard | more than 60 mins.



### 1.1 About the Dataset
This is a dataset with a collection of various cooking recipes, with these attributes : ```name, ingredients, url, image, cookTime, recipeYield, datePublished, prepTime, description.```

### 1.2 Code Outline
**High-level Overview**
* Load Data
* Transform Data
* Filter data
* Difficulty metrics

- - - -

## 3. Special Instructions
Default ```base_dir``` for dataset is ```deepsat-sat6```. Hence, try keeping the notebook and this directory in the same folder. It also the notebook assumes by default that data generated from AWS is stored under  ```fromAWS``` folder. For ease of use, data generated from our experiments from AWS is provided in that directory.

Since, the actual dataset is a space consuming ```(~5.6 GB)```, we have only provided a small set of that dataset, original dataset can be downloaded from the above link of Kaggle which only has ```first 200 rows``` with filenames having suffix ```_200```.





### To run locally
```   

python HelloFresh.py --inputPath input/recipes.json --outputPath output/ --filterColumn ingredients --filterValue beef


```
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
### Required Libraries
You can install necessary packages to run these codes by running the following:
```pip install -r requirements.txt```

## Note
- Make sure install the required [required packages](https://github.com/akshay1996ind/test/blob/master/README.md#required-libraries).

- To running ```HelloFresh.py``` use the [run locally command](https://github.com/akshay1996ind/test/blob/master/README.md#To-run-locally)

- - - -



