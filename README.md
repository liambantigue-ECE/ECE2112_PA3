# ECE2112_PA3
Liam S. Bantigue | 2ECE-A
# EXPERIMENT 3: PYTHON DATA ANALYSIS (PANDAS)
## A. POSITIONAL AND LABEL-BASED SLICING
The problem instructs us to display the shape and complete list of column names of cars, to use positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where the first data row is row 1, and to from cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.

First, to display the shape of the cars, we use the .shape() function that we learned in numpy, the shape is 32 rows and 12 columns. We then display the list of column names using the .columns function to retrieve the column names of the dataframe and then also attach .tolist() function to have a cleaner output compared to the "normal" list() function. <br>

Second, we need to get row 6 - 10 from the dataframe with select column names. To start, we use the variable name _cars_6_to_10_ to assign the function _cars.iloc[]_. This function has the parameters of row index 5 until 10 but not including 10. We use index 5 because PANDAS use 0-based indexing. Now, we use the variable name _column_label_ to have only select column names, we create a column label where all the select columns are enclosed in brackets. Lastly, we assign cars_6_to_10 to a connected cars_6_to_10 and column_label together to ensure cars_6_to_10 only has the specified columns and then display them.<br>
<img width="1362" height="651" alt="image" src="https://github.com/user-attachments/assets/f75e958c-3355-41e0-9582-ad5ffcd6f3b6" /><br>

## B. MODEL LOOKUP
The problem instructs us to use Boolean indexing on the Model column, to display the complete row for Toyota Corolla, and For Pontiac Firebird, display only Model, mpg, hp, and wt.

First, we need to recall our previous PA because that is where we learned how to use Boolean. remember the syntax is that the variable outside means we get the value that is TRUE from the conditions bracketed. the condition is in column name "Model" find the value equal to == "Toyota Corolla". <br>

Second, just like in problem A, we collect the select column names in a bracket and them assign them to variable column_label. We then use the boolean indexing again assigned to variable name pontiac but now for the value equal to == "Pontiac Firebird". We connect pontiac and column_label together with the latter enclosed in brackets and display them. <br>
<img width="885" height="544" alt="image" src="https://github.com/user-attachments/assets/a927d11d-2de2-48f3-9492-c23deb36b2c8" />



## C. MULTI-MODEL SUBSETTING
The problem instructs us to create a DataFrame named selected cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino. Select the rows by their model values rather than by row numbers. Display selected cars and its shape. For these records, retain only Model, mpg, cyl, hp, and gear.

At first I used slicing but as I was typing this READme file I reread the problem and it said to CREATE A DATAFRAME. So, I used the pd.DataFrame() function. To get the data of our DataFrame named selected_cars, instead of typing them manually, we can use the Boolean indexing we just learned to set conditions that automatically gets the required values. The syntax is it gets all TRUE cars values that is equal to the models Datsun 710, Lotus Europa, and Ferrari Dino, since we have multiple values we can use the .isin() function instead of typing multiple OR | in the condition. We then only get the specified column names by using a column label assigned to Model, mpg, cyl, hp, and gear. I also  assigned the specific models needed to a model label named models. This was done to make the code concise and improve readability.

Lastly, we display selected_cars and its shape.<br>
<img width="745" height="423" alt="image" src="https://github.com/user-attachments/assets/b8635c39-327d-48a8-a895-5895fc25a4fe" />
