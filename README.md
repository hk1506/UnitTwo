# UnitTwo
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

#reading file
survey = pd.read_csv('surverydata.csv')
%matplotlib inline

#show the relationship between age and divorced people
#df = pd.DataFrame()

#call divorced column 
plt.scatter(
    x=survey['DIVORCE'],
    y=survey['AGE'],
    color='purple',
    marker='x', s=10)

#show the relationship between number of sibs and the number of kids 
plt.scatter(
    x=survey['SIBS'],
    y=survey['CHILDS'],
    color='purple',
    marker='x', s=10)

#age distribution of the people who took the survey
x = survey['AGE']

#Plot them as a histogram.
plt.hist(x) 
plt.show()

#Subplot of age and number of child.
plt.figure(figsize=(100, 10))

plt.subplot(1, 2, 1)
plt.plot(survey['AGE'], color='purple')
plt.ylabel('Age')
plt.title('Age')

plt.subplot(1, 2, 2)
plt.plot(survey['CHILDS'], color='green')
plt.ylabel('Number of Child')
plt.title('Number of Child ')
plt.show()
