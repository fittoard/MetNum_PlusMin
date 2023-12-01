# TUGAS PROBLEM SOLVING PLUS MINUS DI WEBSTIE HACKERRANK
Kali ini saya akan menjelaskan tentang cara saya mengerjakan tugas yang diberikan oleh dosen saya Anggay Luri Pramana
# QUESTION
Berikut adalah soal yang diberikan dosen saya dalam web bernama HackerRank 
https://www.hackerrank.com/challenges/plus-minus/problem Ini adalah link menuju web Hacker Rank ke tes tersebut 
# METODE-NUMERIK-PLUS-MINUS
METODE NUMERIK SOLVE PLUS-MINUS 


Penyelesaian dari soal ini adalah:
Soal tersebut meminta untuk menghitung proporsi elemen positif, negatif, dan nol dalam sebuah array. Proporsi tersebut harus dicetak dalam desimal dengan 6 tempat setelah titik desimal.

Untuk menghitung proporsi elemen positif, negatif, dan nol dalam sebuah array, kita dapat menggunakan persamaan berikut:
proporsi = jumlah_elemen / total_elemen
Misalnya, jika array tersebut berisi elemen-elemen berikut:
[-4, 3, 9, 0, 4, 1]

Dari 6 elemen tersebut, terdapat 3 elemen positif, 2 elemen negatif, dan 1 elemen nol. Oleh karena itu, proporsi elemen positif, negatif, dan nol dalam array tersebut adalah:
proporsi_positif = 3 / 6 = 0.500000
proporsi_negatif = 2 / 6 = 0.333333
proporsi_nol = 1 / 6 = 0.166667

Jadi, jawaban untuk soal tersebut adalah:
Proportion of positive values: 0.500000
Proportion of negative values: 0.333333
Proportion of zeros: 0.166667

Berikut Codingan untuk soal diatas:
"C++"

#include <bits/stdc++.h>

using namespace std;

string ltrim(const string &);
string rtrim(const string &);
vector<string> split(const string &);

/*
 * Complete the 'plusMinus' function below.
 *
 * The function accepts INTEGER_ARRAY arr as parameter.
 */

void plusMinus(vector<int> arr) {

}

int main()
{
    string n_temp;
    getline(cin, n_temp);

    int n = stoi(ltrim(rtrim(n_temp)));

    string arr_temp_temp;
    getline(cin, arr_temp_temp);

    vector<string> arr_temp = split(rtrim(arr_temp_temp));

    vector<int> arr(n);

    for (int i = 0; i < n; i++) {
        int arr_item = stoi(arr_temp[i]);

        arr[i] = arr_item;
    }

    plusMinus(arr);

    return 0;
}

string ltrim(const string &str) {
    string s(str);

    s.erase(
        s.begin(),
        find_if(s.begin(), s.end(), not1(ptr_fun<int, int>(isspace)))
    );

    return s;
}

string rtrim(const string &str) {
    string s(str);

    s.erase(
        find_if(s.rbegin(), s.rend(), not1(ptr_fun<int, int>(isspace))).base(),
        s.end()
    );

    return s;
}

vector<string> split(const string &str) {
    vector<string> tokens;

    string::size_type start = 0;
    string::size_type end = 0;

    while ((end = str.find(" ", start)) != string::npos) {
        tokens.push_back(str.substr(start, end - start));

        start = end + 1;
    }

    tokens.push_back(str.substr(start));

    return tokens;
}

Berikut Codingan untuk soal diatas:
"python"

def plusMinus(arr):
    positive_count = 0
    negative_count = 0
    zero_count = 0

    for num in arr:
        if num > 0:
            positive_count += 1
        elif num < 0:
            negative_count += 1
        else:
            zero_count += 1

    total_count = len(arr)

    positive_ratio = positive_count / total_count
    negative_ratio = negative_count / total_count
    zero_ratio = zero_count / total_count

    print("{:.6f}".format(positive_ratio))
    print("{:.6f}".format(negative_ratio))
    print("{:.6f}".format(zero_ratio))


if __name__ == "__main__":
    n = int(input().strip())
    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)


    



