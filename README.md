# Gun-and-violence-in-the-US
In this task we are giving a presentation from the gun and violence from the datasets we got from kaggle database. The purpose of this task was to analyse the datasets provided Using python and later come up with a presentation
The presentation is further analysed and posted on public tableau here https://public.tableau.com/app/profile/chilufya.chama/viz/storytellingongunviolence/Story1.
Using python I started by exploring relatinships between gun and violence and later used geographical visualisation in python to analyse which states have the highest number of gun violence.
I later presented the findings in tableau visualisation, made a storytelling and later recommendations on ways to stop gun violence
I have now prepared a power point which I later converted into PDF which I have uploaded here

# Codes used for exploring relationships
For exploring relationship, I used correlation with various visualisation techniques in python whose codes are as follows: 

*creating a correlation matrix with heat map using pandas*
df_selected = df['incident_id', 'No. killed', 'No.injured', 'state_house_district', 'state_senate_district']]
plt.matshow(df_selected.corr())
plt.show()

*creating subplot correlation with matplot using seaborn*
sub = df_selected[['incident_id', 'No. killed', 'No.injured','state_house_district', 'state_senate_district']]
Create a subplot with matplotlib
f,ax = plt.subplots(figsize=(8,8))
*Creating the correlation heatmap in seaborn by applying a heatmap onto the correlation matrix and the subplots defined above*.
corr = sns.heatmap(sub.corr(), annot = True, ax = ax)  The `annot` argument allows the plot to 
place the correlation coefficients onto the heatmap.

*creating correlation using scatterplot*
sns.lmplot(x = 'state_house_district', y = 'state_senate_district', data = df)

*creating correlation using scatterplot*
sns.histplot(df['No. killed'], bins = 20, kde = True)
Add titles and labels (optional)
plt.title('No. of People killed', fontsize=14)
plt.xlabel('Number of people killed)', fontsize=14)
plt.ylabel('Frequency of people killed', fontsize=14)



