Team members:

	Hossein Arjomandi
	Nic Prate
	Tixian Wang
	Zijian Zhen


Problem explanations:
	Data preprocessing:
		1. Area Type and Area use one-hot-encoding;
		2. Year and Month are converted to timestamps;
		3. Take Labor Force as another feature;
		4. Output is Unemployment Rate.

	Data processing:
		1. Question: Each timestamp only has partial observations, how does that work in RNN?
		2. Try just taking California data as input (Debugging test); Or converting all area name to California and see how smaller areas play a role in unemployment rate.
		3. Q: What features should be normalized and how?
		4. Q: Should we treat timestamp as a feature or separately?
		5. Q: What kind of data does RNN taken? Does RNN take both one-hot-encoding and other data type at the same time?
		

Tasks on 10/23/2022:
1st - Zijian: Create a repository with Readme.md as wanted

2nd - Hossein: Convert rows of dataframe to objects of appropriate attributes (one hot encoded, timestamp, integer). Then we have an array of objects

3rd - Nic: See if we can convert this array of objects to a single dataframe

4th - Tixian: See how to pickle an object, be it an array of objects or a dataframe (depending on the answer to 3rd question we may need to pickle a dataframe or an array of objects)



LISCENCE: