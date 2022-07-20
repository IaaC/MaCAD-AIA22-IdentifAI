
![image](https://user-images.githubusercontent.com/97359144/180045584-c28698a4-75d2-4640-93cf-31dc0cd58ea9.png)


By 2050 70% of the population will live in cities, while global temperatures continue to rise and the sealed surfaces of the cityscape continue to increase the heat island effect.

identifAI is an AI tool, that points out potential areas to impact microclimate & reduce urban heat island effects on a street level. It seeks to create mainly awareness among the local residents, experts and the municipality of Vienna. The final and future scope of the project is to make it applicable for cities around the world.
METHODOLOGY
 
![image](https://user-images.githubusercontent.com/97359144/180045717-6356aab0-dfb5-45f3-a988-18e1b04d64b4.png)
General methodology

![image](https://user-images.githubusercontent.com/97359144/180045744-1e87cf3b-204b-43ef-9c4c-0cf46d51d039.png)
Data collection

The data was collected from various open source sources, starting from Open Data Austria, Open Street Maps and specific climatic data from the Central Station for Meterology and Geodynamics and sun radiation values form InFraReD, an AI tool for calculating solar and wind data in cities. The collected data was then appended to street segments through qgis and the python libraries of geopandas.

1. CLUSTERING
We used clustering as a method for identifying the occurring street types in Vienna. Through the kmeans algorithm we were able to understand that the collected data categorized our streets in 18 groups. The clustering method proved to be successful as streets in the same group generally have a similar character, features which we didn’t directly encode. This makes us hopeful that this approach might be used also in other cities aswell.

![image](https://user-images.githubusercontent.com/97359144/180045795-6f3146d9-53d8-440a-bd3a-f2276d342a74.png)
Kelbow visualization

![image](https://user-images.githubusercontent.com/97359144/180045823-f7ed54de-c88b-4d0d-84ed-e2853a286486.png)
Some of the street categories

2. PREDICTING THE UHV INDEX

![image](https://user-images.githubusercontent.com/97359144/180045853-c51ab2e8-aa75-41f4-9c76-b78109957de8.png)
Dataset selection strategy

While trying to predict the UHVI we were confronted with the fact that little correlation was shown between the features and the index. The strategy we followed was to augment the data by interpolating between the min, mean, max bounds of the dataset through SOM – kohonen maps. When testing to the real streets the accuracy results were quite satisfactory.

The  size and features played a key role  in the performance of the model and it performs  accurately as long as  the input  are within the min/max  bounds of our  trained dataset. 

![image](https://user-images.githubusercontent.com/97359144/180045885-86b7531b-e575-462c-a355-56510c2ed765.png)
Linear Regression results

INTERFACE

![image](https://user-images.githubusercontent.com/97359144/180045926-2678a7bc-4ef7-4915-98c0-284a8834db75.png)
Target users

Through a web interface users can access both of our projects. They can see the street category the various streets are assigned to, and also by changing some features understand whether and how it affects the urban heat island vulnerability index.

![image](https://user-images.githubusercontent.com/97359144/180045953-e256336b-dfcd-4f64-b71b-b2ad0b469ec4.png)
Web Interface

CONCLUSIONS – NEXT STEPS
In our opinion the results of our models are promising and can be further improved through the integration of more accurate or additional datasets.
![image](https://user-images.githubusercontent.com/97359144/180045990-2a9a72c5-8784-4cf8-ba67-5ed7febb1b39.png)

 



 

IdentifAI is a project of IAAC, Institute for Advanced Architecture of Catalonia developed in the Master in Advanced Computation for Architecture & Design 2021/22 by students: Erida Bendo, Maria Papadimitraki, Clemens Russ, Mohammad Daniyal Tariq,  faculty: Angelos Chronis and faculty assistants: Serjoscha Düring, Nariddh Khean, Aleksandra Jastrzębska.
