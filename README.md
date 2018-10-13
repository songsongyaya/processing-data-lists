# to create a dictionary of the counts of how many times each country appears in a column in the dataset
#process the first 1000 rows of a file line by line, to create a dictionary of the counts of how many times each country appears in a #column in the dataset. Here, the csv file 'world_dev_in.csv' is available.
(1) firt 1000 rows of a file line by line
with open('world_dev_in.csv') as file:
    # skip the column names
    file.readline()
    # initialize an empty dictionary: 
    counts_dic={}
    # process only the first 1000 rows
    for j in range(1000):
        # split the current line into a list:
        line=file.readline().split(',')
        first_col=line[0]
        if first_col in counts_dict.keys():
            counts_dict[first_col]+=1
        else:
            counts_dict[first_col]=1
print(counts_dict)

(2) Read entire file line by line 
#define a function to read a large file lazily
def read_large_file(file_object):
    while True:
        data=file_object.readline()
        #Break if this is the end of the file
        if not data:
            break:
        else:
            yield data
counts_dict={}            
with open('world_dev_ind.csv') as file:
    for line in read_large_file(file):
        row=line.split(',')
        first_col=row[0]
        if first_col in counts_dict.keys():
            counts_dict[first col]+=1
        else:
            counts_dict[first_col]=1
 print(counts_dict)
        
