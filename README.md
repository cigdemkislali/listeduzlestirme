""" listeduzlestirme
Bir listeyi düzleştiren fonksiyon
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]"""
def flatten_list(nested_list):
    flat_list = []
    for item in nested_list:
        if type(item) == list:
            flat_list += flatten_list(item)
        else:
            flat_list.append(item)
    
    return flat_list

input_list = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
print(flatten_list(input_list))
"""2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]"""
def reverse_list(k):
    k = k[::-1]
    k = [i[::-1] for i in k]
    return k

input=[[1, 2], [3, 4], [5, 6, 7]]


print(reverse_list(input))


