# Week 12 Feedback
Each week, you'll receive a feedback file in GitHub showing a final grade and any specific comments on your assignment, including why points (if any) were deducted.



## Final Score: 8/10

## Assignment 1: Multiple Choice
* 3 pts - You got all the correct answers

## Part 1: Pivoting Data for Fun!
* 1 pts - You got the data filtered down to 1986 - 2015
* 2 pts - You pivoted the data by Year and Status
* 1 pts - You described the plot

## Part 2: Video Conference Usage
* 2 pts - You created the Before and During columns correctly
* 1 pts - You computed the Percent Change correctly

**(-2 pts) This process for calculating the answer and aggregating the data was very convoluted and inefficient.  Anytime you're doing a loop with a Pandas dataframe, you should think again.  You probably mean to be doing an aggregation or some other apply function.**
```python
unique_na=meetings.userName.unique()
for i in unique_na:
  defo=len(meetings[(meetings['startDate'] >= '2020-02-17') & (meetings['startDate'] <= '2020-02-28')&(meetings['userName']==i)])
  duri=len(meetings[(meetings['startDate'] >= '2020-03-16') & (meetings['startDate'] <= '2020-03-27')&(meetings['userName']==i)])
  if defo!=0:
    df=pd.DataFrame({'Before':[defo], 'During':[duri], 'pctChange':[((duri-defo)/defo)],'userName':[i]
  })
    summary=pd.concat([summary,df])
```

## Coding Best Practices:
_Was your code readable, efficient, and in line with what we learned in class?_
* Good variable names?
* Appropriate comments with your code?
* Generally easy to follow and undersand?
