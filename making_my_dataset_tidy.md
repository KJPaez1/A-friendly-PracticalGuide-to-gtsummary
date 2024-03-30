# Making my messy data a tidy data (ready to analyze)
Before to beggin to explore your data, it should have a _standard_ structure that 
is going to make easy the downstream analysis and visualization. In short, 
before you analyse your data, you need to make your data a _tidy data_.

### Refreshing terms and their concepts
There are three terms that are important because all data have them: Observations, Variables, and Values
* Observations are the individuals who are part of your study populations. For example, patients or students.
* Variables are the "things" that you are measuring from your observations. For example, smoking status, or glucose level.
* Values are the possible _answers_ to your variables. For example, for smoking status the answer could be: yes or no; for glucose level (in mg/dL), the answer could be: 95 or 100 

### Data have different looks, but we are only interest in the "good look" (the tidy one)
After data have been collected, it can be structucted in different ways.
The example bellow shows two way in which the same Data can be structured: in data 1 rows observations (patients) and columns are variables; 
in Data 2 thing are inverted, rows are variables and columns are observations. Although this two examples shows the information, the way in which both are structued 
and the way both show the information is not going to make easy to work in RStudio (or in most statistical programs). So we need to make some changes.

![Alt text](https://github.com/KJPaez1/A-friendly-PracticalGuide-to-gtsummary/blob/main/img/data_types.png)

### The look data should have
Apply the following rules to structure your data. If you are starting to collect data, ensure the collection give you a data with the characteristics explained bellow.

#### Rule number 1: Variables are columns and observations are rows
Parafrasing, in a **tidy data** each column is a variable and each rows is a observation. The content among these rows and column would be the values for each observations regarding a specific variable. Figure bellow show graphically this rule.

![Alt text](https://github.com/KJPaez1/A-friendly-PracticalGuide-to-gtsummary/blob/main/img/rule_1.png)

#### Rule number 2: Avoid constant annotations in your values
If your are supposed to show how a variable varies among observations, the value is the only thing to be shown. In other words, avoid including unit measure into your values (for example mg/dL, %, per 1000 people, °C, min, etc). A good practice, would be anotatting the unit measure in the column name or a separated file. Figure bellow shows what to avoid and how to do it.


#### Rule number 3: At collection of data avoid to combine two variables (or more) variables into one 
At least for RStudio, and most statistical programs, you should put just one variable per column. For example, if your variable is Body Mass Index, you will need to collect weight and height, and put them on separated values. You will be able to calculate the BMI, and there is gonna be less change for missing precision. 

#### A side note: for numerical variables, always collect that data as **numerical** (even if you plan to use it as categorical). This will allow you to perform statistical analysis otherwise should not be possible. 


















