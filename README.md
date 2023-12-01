# MetNum_PlusMin
Tugas Problem Solving Plus Minus Di HackerRank
Kali ini saya akan menjelaskan tentang cara saya mengerjakan tugas yang diberikan oleh dosen saya Anggay Luri Pramana

QUESTION
Berikut adalah soal yang diberikan dosen saya dalam web bernama HackerRank image image

https://www.hackerrank.com/challenges/plus-minus/problem Ini adalah link menuju ke tes tersebut jika kalian ingin mencobanya

Disini saya memilih bahasa Python 3 untuk mengenyelesaikan masalah tersebut

Berikut adalah masalah kodingan yang diberikan:

#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    # Write your code here

if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)
ANSWER & EXPLANATION
Seperti yang sudah saya jelaskan diatas bahwa saya menggunakan bahasa Python 3 untuk mengerjakan tugas berikut dan juga import yang saya gunakan dari pilihan diatas adalah import random. Berikut adalah jawaban kodingan saya:

def plusMinus(arr):
    positive_count = sum(1 for num in arr if num > 0)
    negative_count = sum(1 for num in arr if num < 0)
    zero_count = sum(1 for num in arr if num == 0)
    
    n = len(arr)
    
    positive_proportion = positive_count / n
    negative_proportion = negative_count / n
    zero_proportion = zero_count / n
    
    print("{:.6f}".format(positive_proportion))
    print("{:.6f}".format(negative_proportion))
    print("{:.6f}".format(zero_proportion))
Kode ini menghitung jumlah elemen positif, negatif, dan nol dalam array dan kemudian menghitung proporsinya, mencetak setiap proporsi dengan 6 tempat desimal.

Sekarang kita coba untuk gabungkan maka akan menjadi seperti ini

#!/bin/python3
import math
import os
import random
import re
import sys

#
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    # Write your code here
    positive_count = sum(1 for num in arr if num > 0)
    negative_count = sum(1 for num in arr if num < 0)
    zero_count = sum(1 for num in arr if num == 0)
    
    n = len(arr)
    
    positive_proportion = positive_count / n
    negative_proportion = negative_count / n
    zero_proportion = zero_count / n
    
    print("{:.6f}".format(positive_proportion))
    print("{:.6f}".format(negative_proportion))
    print("{:.6f}".format(zero_proportion))
    
if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))
    
    plusMinus(arr)
Input (stdin)
input yang akan di tes dalam web ini ada 2 yaitu:

yang pertama
6
-4 3 -9 0 4 1
yang kedua
8
1 2 3 -1 -2 -3 0 0
Output (stdout)
output yang diinginkan pada setiap input seperti berikut:

yang pertama
0.500000
0.333333
Output yang muncul dari codingan saya adalah

0.500000
0.333333
0.166667
yang kedua
0.375000
0.375000
Output yang muncul dari codingan saya adalah

0.375000
0.375000
0.250000
