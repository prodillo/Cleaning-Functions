# Cleaning-Functions

This notebook contains the class <b>cleaining</b> that has several methods that are useful to clean categorical variables. There is also a <b>Scikit</b> implementation of the methods <b>remove_nulls</b> and <b>group_categories</b> to be used in a pipeline of transformations. The methods are the following:

- <b/>get_nulls(dataframe, columns)</b>: This method returns a dictionary with the percentage of nulls of each columns of a dataframe.
  
    -Inputs:
    
        - dataframe: a pandas dataframe object.
        - columns: the columns of the dataframe to be included in the calculation. If this is not specified all the 
          columns will be taken into account.
          
- <b/>remove_nulls(dataframe, cut_off, columns)</b>: This method remove the columns of a dataframe that have a percentage of nulls higher than a certain cut_off percentage of nulls.

    -Inputs:
    
        - dataframe: a pandas dataframe object.
        - cut_off: The minimum percentage of nulls allowed to keep a columns. If a column has a percentage of nulls higher 
          than the cut_off percentage, it will be removed.
        - columns: the columns of the dataframe to be included in the operation. If this is not specified all the 
          columns will be taken into account.
          
- <b/>fill_nulls(dataframe, label, columns)</b>: This method fill the null values of the columns of a dataframe with a desired label.

    -Inputs:
    
        - dataframe: a pandas dataframe object.
        - label: The text that will be used to replace nulls.
        - columns: the columns of the dataframe to be included in the operation. If this is not specified all the 
          columns will be taken into account.
          
       
- <b/>group_categories(dataframe, cut_off, label, columns)</b>: This method change the category of a categorical variable to a desired label if the percentage of occurence of the category is less than a certain cut_off percentage. This allows to put in the same category those categories with low frequency.

    -Inputs:
    
        - dataframe: a pandas dataframe object.
        - cut_off: Categories with a percentage of occurence less than the cut_off percenatage will be relabeled
        - label: The label for those categories that will be relabeled.
        - columns: the columns of the dataframe to be included in the operation. If this is not specified all the 
          columns will be taken into account.
