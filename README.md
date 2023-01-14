# python_temel_proje

1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:
input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
output: [1,'a','cat',2,3,'dog',4,5]

SOLUTION:

list_1 = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
flattenList = []
def flatten(n):
    for i in n :
        if isinstance(i,list):
            flatten(i)
        else:
            flattenList.append(i)

flatten(list_1)
print(flattenList)

2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:
input: [[1, 2], [3, 4], [5, 6, 7]]
output: [[[7, 6, 5], [4, 3], [2, 1]]

SOLUTION

data = [[1, 2], [3, 4], [5, 6, 7]]
data.reverse()
for i in range(len(data)):
    (data[i])=(data[i])[::-1]

print(data)


www.patika.dev 
