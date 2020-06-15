#step 1 (refer Convert PDFToImage.ipynb)
1.Used Wand to create jpeg for all the pdf files in the test set.

#step 2 (refer ExtractText.ipynb)
1.Used google vission to extract text from pics.
2.Saved all the text from pics to text files.

#step 3 (refer FindTotalAmount.ipynb)
1.I used an observation and listed all the digits in a text file.
2.All the total variables are floating numbers so took the maximum from each list.


 by this approach i got 99.8 accuracy 

I did some anaysis and found out that i can just add all the digits and check if that is present in my list or not
as I was getting error for those bills in which was an option to provide change.

I wrote one small program to check the total of all items and got an accuracy of 99.92.
