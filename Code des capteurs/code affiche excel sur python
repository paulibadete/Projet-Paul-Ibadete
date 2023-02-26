import xlrd
import pandas as pd
workbook = xlrd.open_workbook_xls("exempletableau.xls", ignore_workbook_corruption=True)
data = pd.read_excel(workbook)
df = pd.DataFrame(data)
derniereligne=df.iloc[len(data)-1]
print(data)
#print("///////")
#print(len(data))
#print("///////")
print(derniereligne)
#print(df.shape)
