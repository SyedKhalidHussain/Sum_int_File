# Sum_int_File
#Sum of numbers in a File

import re
File = input('Enter a file:')
fname = open(File,'r')
print(sum([int(i) for i in re.findall('[0-9]+',fname.read()) ]))
