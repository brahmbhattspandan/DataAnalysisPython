# Midterm Exam - Spring 2017 

- Total Points : `100`
- Deadline : `March 6th, 11:59 PM`
- Submission type : `Markdown document + Ipynb Notebook`

---

### Question 1 : (45 Points)

> Using Enron data-set, perform **3**  analysis.

**15 points per analysis**

#### Instructions :
- [Enron Scandal Summary](http://www.investopedia.com/updates/enron-scandal-summary/) - Link to Investopedia article to get a brief summary about the what the scandal was.
- The enron data-set is available at [CMU Enron data 1.82 GB tgz file](https://www.cs.cmu.edu/~./enron/enron_mail_20150507.tgz) . 
- **`You do not need to upload this data in your repository`**.  TA will have their own local copy of the  data at `~/midterm/data/enron/maildir/*`. So use this relative path for storing your data.
```sh
$ mkdir -p ~/midterm/data/enron/
$ cd ~/midterm/data/enron/
# Download it manually (faster) and unzip it or use below command (slower)
$ curl -O https://www.cs.cmu.edu/~./enron/enron_mail_20150507.tgz
```
- You can do any analysis of your choice. A better analysis is one which gives useful information. 




---
### Question 2 : (55 points)


> Use NYT API to collect NYT data. Perform 3 analysis on the collected data.

Link to NYT developer docs : [NYT API Documentation](http://developer.nytimes.com/)


| Code        | Points           | 
| ------------- |:-------------:| 
|Collect Data       | **10** Points | 
| Storing Data      | **15** Points      |   
| Individual Analysis  | **10** Points      |  

#### Instructions :
- You would need to create an API key.
- Use `request` or `beautiful-soap` library to download the data. (No other library or crawler allowed).
- Store the data in your local machine.
- Your analysis should use **this downloaded data only** (and not try to redownload this data again during analysis time).
-  There is a rate limit for downloading the data. I would suggest you to start collecting the data from day 1. You can try using multiple account to get more than 1 key.
-  You need to use atleast 2 API method eg: `archive`, `Article Search`. **Do not use** `Movies Review`, `Semantic` API.

---

# General Instructions :

- You need to submit a `runnable ipython notebook`. TA should be able to clone your repository and run the code in their machine. (They will install any libraries you have as well as set-up any environment variable and file argument that you have need.) But there should be no code change required to run the notebook.
- You are allowed to use any python libraries except **Numpy,Pandas,automated crawler tools**. You can use a library for crawling (if you think you need it but it should not be an automated click to run types.)
- Do not share/upload any keys on Github. You should store them as environment variable.
```sh
$ export nyt_archive_key = abcd1234
```
```python
import os
nyt_archive_key = os.get_env('nyt_archive_key')
```
- You can only use excel,matplotlib,seaborn to create plots (**optional to create plots**).
- Following folder/file structure is preferred


| Path        | Purpose           | 
| ------------- |-------------| 
|`midterm/`       | folder to store all your midterm submission files | 
| `midterm/data/*`      | Store all raw data      |   
| `midterm/que[1-2]/ana_[1-3].ipynb`  | Notebook to store the code for analysis      |
| `midterm/que[1-2]/ana_[1-3]/`  | Extra files required/generated for each analysis (Eg. output.csv,plot.png)      |
| `midterm/readme.md`  | Markdown report     |

-  The TA will only look for a folder `midterm` in your repository and all the required files should be available inside it. You may lose points if the files are kept in some other location.
-  Using **NLTK** in your analysis will carry higher points. Just using it for the sake of it does not constitute as NLTK usage.
-  Since this is mid-term, **no extension of deadline is available**. You lose 5 point for every 4 hours delay. Eg : `You submit it at 12:01 AM or 3:01 AM , you will lose 5 points. You submit it at 4:01 AM you lose 10 points`
-  Please use **Markdown syntax in your ipynb notebook** so the TA understands what you are trying to do. 
-  You will need to create a final report stating what analysis you have done and its output. It needs to be created as a markdown document as named `readme.md`. This is important and failing to do so will result in large loss of marks. **`No Prezi,ppt,pdf allowed`**. Imagine if I was to go through only this document (and no other file), I should be able to understand what data you had, how you obtained it, how is it stored, what analysis have you done, what information did you get etc etc.