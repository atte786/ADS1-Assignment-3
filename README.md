# ADS1-Assignment-3
"creating a function for data normalization"
def normlz(data):
    nm=normalize(data)
    return nm
cc = ['TUR','CHN','ISR','MLI','NGA']
ind1=["EN.ATM.CO2E.KT"]
ind1mn=['C02 Emission']
ind2=["EG.ELC.COAL.ZS"]
ind2mn=['Electricity production from coal source']
my_dataframe1  = wb.data.DataFrame(ind1, cc, mrv=50).T
my_dataframe1=my_dataframe1.fillna(my_dataframe1.mean())
my_dataframe1.head()
