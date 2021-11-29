# High school student alcohol consumption data analysis

This data analysis work has been made for my application as a PhD student for the ExpBoD.
Its purpose is to show how I compute and interpret data, while giving a sample of redaction in English.
This doesn’t follow the usual research paper structure. The introduction is minimal, and results and discussion are mixed up. I tried to be as concise as possible while still showing the relevant insight we could extract from the given database.
This work could have been more exhaustive, but:
- I didn’t want it to be too long so that it could be at least partially read during an application selection process
- I wanted to finish this work before the 1st of December deadline
- I didn’t want to be too elusive on the findings that were already at reach on this first analysis

# Files description

- Report.doc : The data analysis report in itself. It includes essential graph and charts, but you will need to navigate through the notebooks for an exhaustive knowledge of the data and the method

- Only_essential_cells.ipynb : The "clean" data analysis notebook with only the final models and data processing, without all the steps. I personnaly suggest to keep this open while reading the report in order to check any given information

- Step_by_step_procedure.ipynb : The "messy" version of the previous notebook. It includes every relevant tests and notes to understand how data was computed and the models discarded or kept. It can be interesting to take a look (especially at the notes in each cell) if you really want to have a deeper understanding of the method. Still, it is too messy to be relevant when trying to navigate along with the information in the report, so I suggest to take a look at this notebook only to check the method, and to use the other notebook for the report reading. 

- student-mat.csv & student-mat.csv : both data files from the dataset available here https://www.kaggle.com/uciml/student-alcohol-consumption?select=student-mat.csv If you want to make a data analysis by yourself, be careful with the data join as there are duplicates between the two files. Here is the command for the join :  pd.concat([pd.read_csv('student-mat.csv'), pd.read_csv('student-por.csv')], ignore_index=True)\            .drop_duplicates(["school","sex","age","address","famsize","Pstatus","Medu","Fedu","Mjob","Fjob","reason","nursery","internet"])
