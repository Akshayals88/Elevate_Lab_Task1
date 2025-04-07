 Customer Personality Analysis :-

 Notes:-
** First **

 I have imported  the data in jupyter notebook using pandas lib using this command like:-
 
 import pandas as pd

df = pd.read_csv("marketing_campaign.csv")
print(df.head(10))

**Second **

print(df.isnull())  By using this code i can easily find out the null values. That is there any null values or not ..
if the values are false its mean that this particular column did not have any null values.

**Third**

I have to convert the column name **Dt_Customer** to correct date formate like 'dd-mm-yyyy' formate 
soo that i have wrote this code 
df['Dt_Customer'] = pd.to_datetime(df['Dt_Customer'], format='mixed', dayfirst=True)
This line converts the Dt_Customer column into proper datetime objects, even if the dates are in mixed formats — and sets the format to assume day-first format, like dd-mm-yyyy.

df['Dt_Customer'] = df['Dt_Customer'].dt.strftime('%d-%m-%Y')


**fourth**

df.columns = df.columns.str.strip().str.lower().str.replace(' ', '_').str.replace(r'[^\w]', '', regex=True)
This code task is to convert all the given columns into the lower case or small Letter..


