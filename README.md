# import libraries 
import pandas as pd
import matplotlib.pyplot as plt 
import glob
# assign a constant figure size and use it in plotting to make plots larger
FIG_SIZE = (8,6)
# get all filenames under the data directory 
l = [pd.read_csv(filename) for filename in glob.glob("./data/*.csv")]
# check the list size to understand how many files will be read
# should be equal to 50
print(len(l))
#  create the dataset using all files under the data directory
df = pd.concat(l, axis=0)
df.head()
