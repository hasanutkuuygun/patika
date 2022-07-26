# Merge Sort
www.patika.dev

# Soru 1
[16,21,11,8,12,22]

- Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.

Merge Sort yöntemine göre dizi her adımda ikiye bölünerek tek bir eleman kalana kadar bölme işlemine devam edilir. Daha sonra birleştirme işlemi yapılır. Sıralama işlemi elemanlar birleştirilirken yapılmaktadır.

                                            [16,21,11,8,12,22]
                                            /                 \
                                        [16,21,11]          [8,12,22]
                                        /         \        /         \     
                                    [16,21]      [11]   [8,12]       [22]
                                    /     \        |    /    \        | 
                                  [16]   [21]    [11]  [8]   [12]    [22]
                                   \      /        |     \    /        |
                                     [16,21]     [11]    [8,12]       [22]
                                         \        /         \          /
                                          [11,16,21]          [8,12,22]
                                               \                   /
                                                 [8,11,12,16,21,22]
 
- Big-O gösterimini yazınız.
Big-O &rarr; O(nlogn)