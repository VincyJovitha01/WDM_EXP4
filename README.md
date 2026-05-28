### EX-4: Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 23/05/2026
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
#### NAME : VINCY JOVITHA V
#### REG NO: 212223230242
```
import pandas as pd
df = pd.read_csv("C:/Users/admin/Desktop/Web-Data-Mining/clustervisitor.csv")
df

cluster = { 'Young ': (df['Age']<=30) , 'Middle':((df['Age']>30) & (df['Age']<=50)), 'Old':(df['Age']>50) }
count=[]
for g ,v in cluster.items():
    visitor= df[v]
    print(f"The Visitor in {g} Group are \n", visitor)
    print("count = ", len(visitor))
    count.append(len(visitor))

    
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plt.bar(cluster.keys(), count, color = 'skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitor')
plt.title('Visitor Distribution Across Age Groups')
plt.show()
```
### Output:

<img width="369" height="668" alt="image" src="https://github.com/user-attachments/assets/8632fe14-a1ad-44dc-8133-ae18078f85e9" />


### Visualization:

```
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plt.bar(cluster.keys(), count, color = 'skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitor')
plt.title('Visitor Distribution Across Age Groups')
plt.show()

```
### Output:
<img width="893" height="632" alt="image" src="https://github.com/user-attachments/assets/63282546-4740-4aee-822a-5860431800ca" />

### Result:
Thus the cluster and visitor segmentation for navigation patterns was implemented successfully in python.

