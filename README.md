This repository contains three Jupyter notebooks plus some schema files used to create our Feature Groups. The purpose of the notebooks is described as:

•	1_generate_creditcard_transactions.ipynb : generates raw transaction data for credit cards and consumers </br>
•	2_create_feature_groups.ipynb : creates two feature groups used to store aggregate features for consumer data and credit card data </br>
•	3_fs_get_historical_features.ipynb: creates the periodic snapshots of aggregate data, writes them to the Feature Store, creates the entity dataframe, and creates and executes the point-in-time queries </br>

Instance Types: </br>
Please note our recommendation about instance types. To run the various **Spark Dataframe** operations (like `foreachPartition`, and `reduceByKey`), notebook 3 configures non-default parameters for the Spark session object. To run this notebook properly, we recommend
 using an instance type that allocates at least **32 GB RAM**. We have successfully tested these notebooks on the following instance
types: `ml.c5.4xlarge`, `ml.m5.4xlarge`.

