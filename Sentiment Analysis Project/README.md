Datasets need to be uploaded/called for the .ipynb files to run.
●	Datasets:

1.	Original Dataset with no emojis
a.	emotions1 - emotions1.csv - For Baselines, CNN and LSTM
b.	emotions1 - emotions1.xlsx - For BERT and XLNET
2.	Dataset with Emojis as is
a.	Final_Emojis - emotions1.csv - For Baselines, CNN and LSTM
b.	Final_Emojis - emotions1.xlsx - For BERT and XLNET
3.	Dataset with Emojis converted to words
a.	Dataset_With_Emoji.csv - For Baselines, CNN and LSTM

●	Models:

1.	Baseline Models 
- 	Both 1a and 3a should be present locally to get the  output of the Baseline models with and without emojis.
a.	Baselines - Baseline.ipynb 
2.	CNN
-	Both 1a and 3a should be present locally to get the output of CNN with and without emojis.
a.	CNN without using word2vec - CNN with word2vec.ipynb
b.	CNN using word2vec - CNN with word2vec.ipynb

3.	LSTM
      -	The ipynb file is called LSTM.ipynb (this includes all combinations of LSTM embedding layers and is also the file that contains Word2vec+Emoji2vec on CNN) ; Files to be present locally are
	     -	Emoji2vec.bin
	     -	Phrase2vec.py
	     -	The 3 datasets mentioned above


4.	BERT 
-	By default emoticons to words mapping is enabled. To disable it, comment cell 11 (apply(token_emoji_conversion) method). 
-	Mount the drive (helpful in saving checkpoints too) and make sure that dataset is at “/content/gdrive/My Drive/Final_Emojis - emotions1.csv” location.
-	Use GPU for code execution 
-	Specify checkpoint directory under - OUTPUT_DIR in code
a.	BERT for cased - BERT_converting emoji to word_cased.ipynb; the generated probabilities are saved on the drive in a .csv file named prob_uncased.csv
b.	BERT for uncased - BERT_converting emoji to word_uncased.ipynb; the generated probabilities are saved on the drive in a .csv file named prob_cased.csv

c.	BERT(cased+uncased) - read cased and uncased csv files in variables cased_prob and uncased_prob in the code. 


5.	XLNET
-	Mount the drive and make sure that dataset is at the “/content/gdrive/My Drive/Final_Emojis - emotions1.csv” location.
-	Specify path from which checkpoint is to be loaded in torch.load
-	Use GPU for code execution 
-	Follow instructions specified in XLNet.pynb notebook.
a.	For XLNet - XLNet.ipynb
