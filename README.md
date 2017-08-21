# Sum_int_File
#Sum of numbers in a File

import re
value = 0
count = 0
File = input('Enter a File:')
fname = open(File,'r')
for line in fname:
  list = re.findall('[0-9]+',line)    
  count = count + len(list)    
  if len(list) == 0:continue    
  #print(list)
  for i in range(len(list)):
    num = int(list[i])        
    value = value + num
  
 print("There are %d values with a sum equls to %d:"% (count,value))
