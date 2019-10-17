Requirements
python 3.*
numpy
pandas
scipy

<br>
Input and output
Input
Ratings and side information are able to be given as input.<br>
All the input should be given as tab-separated files.<br>
Rating file should have three columns for user_id, item_id, and rating.<br>
User_id should not overlapped with item_id.<br>
Side information file should have two columns for user/item_id and value.<br>
The name of rating files should be 'rating.tsv'.<br>
Output
We print out Spearman's rho, precision@k, and recall@k with stdout.<br>
You may write log generator for the results for yourself.<br>
Intermediate outputs<br>
We generate intermediate outputs such as vectors and biases of users and items.<br>
All the intermediate outputs have their file names under the rule: 'method name_dataset name_parameters_fold.txt'.<br>

The hyperparameters you can give are as follows.<br>

argument_type	default argument_value	details<br>
--dataset	filmtrust	Name of dataset<br>
--method	MF_exp	Name of method (*1)<br>
--data_path	'../data/'	Where datasets are<br>
--input_path	'../data//input/'	Where inputs are<br>
--result_path	'../results'	Where intermediate results are<br>
--is_social	True	Whether social links are used<br>
--lr	0.05	Learning rate<br>
--lamb	0.3	Regularization parameters<br>
--dim	5	Dimension of vectors<br>
--is_sample	False	Wheter to sample seed users<br>
--num_seed	300	# sampled seed users<br>
--c	0.2	Probability of restart<br><br>
--beta	0.4	Probability of walk in RWR_bias<br>
--gamma	0.3	Probability of restart in RWR_bias<br><br>
--delta	1.0	Weight of additional links in RWR_side<br>

