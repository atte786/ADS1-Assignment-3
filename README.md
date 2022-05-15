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
my_dataframe2  = wb.data.DataFrame(ind2, cc, mrv=50).T
my_dataframe2=my_dataframe2.fillna(my_dataframe2.mean())
my_dataframe2.head()
clmns=my_dataframe1.columns
clrs="rmkby"
for i in range(len(clmns)):
    plt.figure(figsize=(6,3))
    plt.title('C02 Emission by Country for {}'.format(clmns[i]))
    plt.plot(my_dataframe1[clmns[i]],"{}D-".format(clrs[i]),label=clmns[i])
    plt.xlabel("Year")
    plt.xticks(rotation=90)
    plt.ylabel("C02 Emission")
    plt.legend(loc="best")
    plt.grid()
    plt.show()
