# English_Premier_league_Analysis_and_Prediction
Predicting the final winner of Season using spark, python, tableau for visualisation

English Premier League Dataset Project.

Dataset_Source: https://www.kaggle.com/crained/english-premier-league-football
                https://www.kaggle.com/irkaal/english-premier-league-results
                https://www.kaggle.com/aslambaig/premier-league-fixtures-2021/download
                https://www.kaggle.com/aslambaig/english-premier-league-player-goals/download
                https://www.kaggle.com/aslambaig/english-premier-league-player-assists/download

Required Software:
1. MongoDB Compass
2. Jupyter Notebook (pyspark)
3. Tableau


General Steps :

	1. Unzip the attached folder 'Data_603_EPL_Folder' which contains the ipynb file 'Data_603_EPL_Final_Project' and the remaining datasets which have been attached into that folder
	2. Open the jupyter notebook and load the above mentioned file 'Data_603_EPL_Final_Project'.


MongoDB Steps:

	1. In this project, we use MongoDB for high volume storage. (Download MongoDB using the link:- https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
	2. From the unzipped Data_603_EPL_Folder find the json_files folder.
	3. Copy the path of the folder.
	4. Then we load the data to MongoDB using the following commands in command prompt:
      
      	     1. cd C:\Program Files\MongoDB\server\4.4\bin      (Change the path based on the location of MongoDB bin folder)

	     2.Then using the below command load all the json files into MongoDB 
               for %i in (C:\Users\venkata\Downloads\json_file\*) do mongoimport --file %i --jsonArray --db EPL_DB --collection %i 
		(Change the path 'C:\Users\venkata\Downloads\json_file\*' with file path that you have copied above i.e., json_files folder)

	5. Check whether all the files data is loaded into MongoDB as collections or not
    
	6. After loading all the .json files into MongoDB as collections we move ahead with next steps. 



Jupyter:

	1. First, we load the data into jupyter from mongodb and load each collection and convert them to dataframe.
	2. Install the packages like pymongo, pyspark, tensorflow before executing any codes using the below commands
		pip install pymongo
		pip install pyspark
		pip install tensorflow
		pip install sklearn
	3. Now we are all set to go ahead with the code, start running the code cells one by one to get the outputs.
