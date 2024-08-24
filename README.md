# Solar_Energy_Production_Zone-Clustering

## Objective:
The goal of this project is to make use of data that provides details on current solar power installations in the target region. Our objective is to o group (cluster) geographical areas according to their total energy production by means of this data analysis.

## Data Wrangling

- The shape of the dataset are 218115 rows and 17 columns.
- Dropped the Project ID, Zip, Circuit ID, Energy Storage System Size (kWac), Division, and Substation columns because some of the columns had the largest number of null values and some of the columns are not relevant for the analysis.
- Extracted month from Interconnection Date column and Data Through Date column.

## Exploratory Data Analysis

![image](https://github.com/user-attachments/assets/b9db2f72-3b46-4186-a226-f083d62bdfc2)

- Staten Island City has the highest frequency, exceeding 10,000 occurrences.
- Brooklyn ranks second in frequency but falls slightly behind Staten Island.
- Baldwin City records the lowest frequency among the observed locations.

![image](https://github.com/user-attachments/assets/b8e2373e-09f1-4535-845d-054e334f2c29)

- Suffolk County emerges as the most frequent county, with a frequency exceeding 50,000.
- Nassau County follows closely, with a frequency ranging between 30,000 and 40,000.
- Columbia County exhibits the lowest frequency among all counties surveyed.

![image](https://github.com/user-attachments/assets/5cd70df5-723c-42e2-b4cb-a68569fc500e)

- Used scatter plot to see the linear relationship between PV system size (kWac) and estimated annual PV energy production (kWh).
- The presence of outliers are influencing the relationship between PV system size and estimated annual PV energy production.

![image](https://github.com/user-attachments/assets/b2e53d29-2e1d-4d23-ac02-92f1f3501745)

- Used the scatter plot to see the linear relationship between PV system size (kWac) and estimated annual PV energy production (kWh).
- After Removing the Outliers, It is showing me the linear relationship between both the columns.

![image](https://github.com/user-attachments/assets/61be5519-60e9-4643-b7e5-8f8915f13605)

- Distribution of Estimated Annual PV Energy Production (kWh): The distribution is multimodal with peaks around 5,000 and 10,000 kWh,indicating common system sizes, but shows a significant increase at 20,000 kWh.
- Distribution of PV System Size (kWac): The PV system size in kWac has multiple peaks, notably around 5 kWac, suggesting common installations around this size, with a large spike at 15 kWac.
- Distribution of Estimated PV System Size (kWdc): The system size in kWdc mirrors the kWac distribution, with multiple peaks around 5 to 7 kWdc, and a sharp rise at around 17.5 kWdc.

![image](https://github.com/user-attachments/assets/d6ff69df-7dc2-43e9-a164-e6bef811f7b3)

- December month has Peaks in frequency with higher interconnection rates as compare to other months.

## Scaling (Normalization)
![image](https://github.com/user-attachments/assets/56dc2e74-c21f-4116-b154-ff103ba9ad36)
![image](https://github.com/user-attachments/assets/2530fa1e-dab5-42d5-bba0-9a1295342978)

## Plotting the Elbow Curve

![image](https://github.com/user-attachments/assets/2ecc8e46-651c-472d-97e6-c86f2b2eacd0)
- Based on the elbow method, 3 appears to be the most suitable number of clusters for the given dataset.
- This insight can guide further analysis and decision-making processes, such as segmenting data into distinct groups for targeted actions or understanding underlying patterns within the data.


![image](https://github.com/user-attachments/assets/6f4566dc-6005-4fdd-a57c-9821cb3bffe4)

![image](https://github.com/user-attachments/assets/e16c4194-ab46-47ed-ba26-98348d256474)

![image](https://github.com/user-attachments/assets/95954179-eae0-4e62-95f3-a5df11cdf11a)

- The linear grouping and placement of centroids suggest that the algorithm effectively separates the data into three clusters based on their feature values.

## Conclusion:
- The addition of the 'Cluster' and 'Segment' columns enables the DataFrame to categorize each data point into meaningful segments based on the clustering results.
- In the higher zone, the estimated annual PV energy production is the highest at 18.67k, followed by 11.32k in the lower zone and 6.12k in the moderate zone.
- The average PV system size in the higher zone is the highest among all zones, indicating larger solar installations in this area.
- In December, all annual PV energy production occurs, indicating that December is a significant month for solar energy production, potentially due to favorable weather conditions or operational factors.

