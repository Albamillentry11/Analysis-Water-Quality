# Analysis Water Quality Data #
## Context of the Data
Access to safe drinking-water is essential to health, a basic human right and a component of effective policy for health protection. This is important as a health and development issue at a national, regional and local level. In some regions, it has been shown that investments in water supply and sanitation can yield a net economic benefit, since the reductions in adverse health effects and health care costs outweigh the costs of undertaking the interventions.
## Data Understanding
* Source Data: https://www.kaggle.com/adityakadiwal/water-potability
* Data Dictionary from the explanation of the column in the data:
1. pH value: PH is an important parameter in evaluating the acid–base balance of water. It is also the indicator of acidic or alkaline condition of water status. WHO has recommended maximum permissible limit of pH from 6.5 to 8.5. The current investigation ranges were 6.52–6.83 which are in the range of WHO standards.
2. Hardness: Hardness is mainly caused by calcium and magnesium salts. These salts are dissolved from geologic deposits through which water travels. The length of time water is in contact with hardness producing material helps determine how much hardness there is in raw water. Hardness was originally defined as the capacity of water to precipitate soap caused by Calcium and Magnesium.
3. Solids (Total dissolved solids - TDS): Water has the ability to dissolve a wide range of inorganic and some organic minerals or salts such as potassium, calcium, sodium, bicarbonates, chlorides, magnesium, sulfates etc. These minerals produced un-wanted taste and diluted color in appearance of water. This is the important parameter for the use of water. The water with high TDS value indicates that water is highly mineralized. Desirable limit for TDS is 500 mg/l and maximum limit is 1000 mg/l which prescribed for drinking purpose.
4. Chloramines: Chlorine and chloramine are the major disinfectants used in public water systems. Chloramines are most commonly formed when ammonia is added to chlorine to treat drinking water. Chlorine levels up to 4 milligrams per liter (mg/L or 4 parts per million (ppm)) are considered safe in drinking water.
5. Sulfate: Sulfates are naturally occurring substances that are found in minerals, soil, and rocks. They are present in ambient air, groundwater, plants, and food. The principal commercial use of sulfate is in the chemical industry. Sulfate concentration in seawater is about 2,700 milligrams per liter (mg/L). It ranges from 3 to 30 mg/L in most freshwater supplies, although much higher concentrations (1000 mg/L) are found in some geographic locations.
6. Conductivity: Pure water is not a good conductor of electric current rather’s a good insulator. Increase in ions concentration enhances the electrical conductivity of water. Generally, the amount of dissolved solids in water determines the electrical conductivity. Electrical conductivity (EC) actually measures the ionic process of a solution that enables it to transmit current. According to WHO standards, EC value should not exceeded 400 μS/cm.
7. Organic_carbon: Total Organic Carbon (TOC) in source waters comes from decaying natural organic matter (NOM) as well as synthetic sources. TOC is a measure of the total amount of carbon in organic compounds in pure water. According to US EPA < 2 mg/L as TOC in treated / drinking water, and < 4 mg/Lit in source water which is use for treatment.
8. Trihalomethanes: THMs are chemicals which may be found in water treated with chlorine. The concentration of THMs in drinking water varies according to the level of organic material in the water, the amount of chlorine required to treat the water, and the temperature of the water that is being treated. THM levels up to 80 ppm is considered safe in drinking water.
9. Turbidity: The turbidity of water depends on the quantity of solid matter present in the suspended state. It is a measure of light emitting properties of water and the test is used to indicate the quality of waste discharge with respect to colloidal matter. The mean turbidity value obtained for Wondo Genet Campus (0.98 NTU) is lower than the WHO recommended value of 5.00 NTU.
10. Potability: Indicates if water is safe for human consumption where 1 means Potable and 0 means Not potable.
## Data Cleansing
* Check for each column and find if any column is redundant or useless.
* Check for missing values.
* Check for outliers.
* Check if the data format is already suitable for algorithm.
* Check for value that are not consistent with general common sense.
## Exploratory Data Analysis (EDA)
* ### Check simple statistic of the numeric value
![image](https://user-images.githubusercontent.com/46348831/128813882-a2682b91-3aa8-43a2-a85c-e3a854454b4e.png)
From the data shows the distribution of the analyzed data from the data file water_potability.csv by showing the level
* ### Check Outlier Using Boxplot
![image](https://user-images.githubusercontent.com/46348831/128814535-58187ff0-2fa4-41b6-b445-04ed2af6aa0d.png)

## Principal Component Analysis (PCA)
![image](https://user-images.githubusercontent.com/46348831/128816016-eb511d93-bebc-4997-a6fc-9458e65d9f66.png)
The results of the visualization of the data that have been used are then described into a 2D plot that will display the distribution of the data plot as shown in the figure. These results describe the results of the processed data and explain that the plot shows the purple color as potability 0 or undrinkable water and yellow as number 1, which is drinkable water from the analysis of the data from the table.
## Clustering
* ### Check Using Elbow Method
![image](https://user-images.githubusercontent.com/46348831/128815623-bcf9c737-3add-48f5-a78f-8564cb903553.png)
The results of the tests carried out using the Elbow Method provide an indication that the analysis from the 1 - 30 range illustrates that the 3rd point is the most optimal because it has an inertia drop value which has a stable value at its distance and is regular (does not have a distance range). far away). The claustering time on the graph also shows the calculated time of python with a stable rhythm.
* ### Plot Using PCA Using the Best Cluster
![image](https://user-images.githubusercontent.com/46348831/128815810-848b33f9-2ac5-43af-bce3-1a67b57570db.png)
The plot results explain that the level of data distribution from the PCA visualization results has a small data similarity so that it produces a plot like the picture because the data visualization results from the water_potability.csv table have numerical proximity.
