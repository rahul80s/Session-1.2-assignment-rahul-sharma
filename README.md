# Session-1.2-assignment-rahul-sharma
Acagild session 1.2 assignment
1. What should be the output of the following script?
   v <-c(2.5.5,6)
   t <-c(8,3,4)
   print(v%/%t)

Ans 1.  ->  0 1 1

2. You have 25 excel files with names as xx_1.xlsx, xx_2.xlsx,....xx_25.xlsx in a dir. Write a program to extract the contents of each sheet
and make it one df.  

Ans 2. ->
write.xlsx(x, file, sheetName="Sheet1", 
  col.names=TRUE, row.names=TRUE, append=FALSE)
write.xlsx2(x, file, sheetName="Sheet1",
  col.names=TRUE, row.names=TRUE, append=FALSE)
write.xlsx3(x, file, sheetName="Sheet1",
  col.names=TRUE, row.names=TRUE, append=FALSE)
  .....
  .....
write.xlsx25(x, file, sheetName="Sheet1",
  col.names=TRUE, row.names=TRUE, append=FALSE)
 
3. If the above 25 files were csv files, what would be your script to read?

Ans 3. -> 
  f<is.files(pattern='*.csv')
  of<f%>%map_df(read_excel)
