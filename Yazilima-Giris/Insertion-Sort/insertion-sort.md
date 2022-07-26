# Insertion Sort
www.patika.dev

# Soru 1
[22,27,16,2,18,6]

**1. Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.**
    **Aşama 1:** Verilen dizideki en küçük değer olan 2 sayısını buluruz. Bu sayıyı dizinin ilk indeksinde bulunan 22 sayısı ile yer değiştiririz.
    [22,27,16,2,18,6] &rarr; [2,27,16,22,18,6]
    **Aşama 2:** Aşama 1'de elde edilen yeni dizi baz alınır ve ilk indeksten sonra gelen sayılardan en küçüğü olan 6 sayısını buluruz. Bu sayıyı dizinin ikinci indeksinde bulunan 27 sayısı ile yer değiştiririz.
    [2,27,16,22,18,6] &rarr; [2,6,16,22,18,27]
    **Aşama 3:** Aşama 2'de elde edilen yeni dizi baz alınır ve ikinci indeksten sonra gelen sayılardan en küçüğü olan 16 sayısını buluruz. Bu sayıyı dizinin üçüncü indeksinde bulunan sayı ile değiştirmemiz gerekmektedir. Ama 16 sayısı hali hazırda üçüncü indekste bulunduğu için dizide herhangi bir değişiklik olmayacaktır.
    [2,6,16,22,18,27] &rarr; [2,6,16,22,18,27]
    **Aşama 4:** Aşama 3'te elde edilen yeni dizi baz alınır ve üçüncü indeksten sonra gelen sayılardan en küçüğü olan 18 sayısını buluruz.Bu sayıyı dizinin dördüncü indeksinde bulunan 22 sayısı ile yer değiştiririz.
    [2,6,16,22,18,27] &rarr; [2,6,16,18,22,27]
    **Aşama 5:** Aşama 4'de elde edilen yeni dizi baz alınır ve dördüncü indeksten sonra gelen sayılardan en küçüğü olan 22 sayısını buluruz. Bu sayıyı dizinin beşinci indeksinde bulunan sayı ile değiştirmemiz gerekmektedir. Ama 22 sayısı hali hazırda beşinci indekste bulunduğu için dizide herhangi bir değişiklik olmayacaktır.
    [2,6,16,18,22,27] &rarr; [2,6,16,18,22,27]

Böylelikle (n-1) kadar işlem yapılmış olduğumuzda sıralama işlemimiz tamamlanmış olmaktadır.

**2. Big-O gösterimini yazınız.**

Insertion Sort sıralama yöntemini anlamak için dizide n kadar sayı bulunduğu göz önüne alalım. Eğer dizideki tüm elemanlar sıralı bir şekilde ise (best case) baştan başlayarak tüm sayıları kontrol ettiğimizde n kadar sayıyı kontrol etmiş ve işlemi tamamlamış oluruz. En iyi durumu incelediğimiz bu örnekte insertion sort için Big-O gösterimi:
- Best Case &rarr; o(n)

Dizideki elemanların sıralı olmadığı diğer durumlar için ise ilk seferde n kadar sayıyı kontrol edip en küçüğünü bulduktan sonra, ikinci sefer ilk sayı hariç yani (n-1) kadar sayıyı kontrol etmemiz gerekmektedir. Bu işlemleri son sayıya kadar tekrarladığımızda aşağıdaki ifade kadar işlem yapmamız gerekmektedir:

n + (n-1) + (n-2) + ... + 1 = [n*(n+1)/2] = (n<sup>2</sup>+n)/2 

Big-O gösteriminde domine fonksiyon ele alındığı için average ve worst case için Big-O gösterimi:
- Average Case &rarr; o(n<sup>2</sup>)
- Worst Case &rarr; o(n<sup>2</sup>)

**3. Time Complexity: Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.**

Average Case: Aradığımız sayının ortada olması &rarr; [22,27,16,2,18,6]

Worst Case: Aradığımız sayının sonda olması &rarr; [27,22,18,16,6,2]

Best Case: Aradığımız sayının başta olması &rarr; [2,6,16,18,22,27]


**4. Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.**

18 sayısı sıralama yapıldıktan sonra dizinin ortasında bulunacaktır. Bu sayı dizinin ilk halinde de dizinin ortasında bulunduğu için **average case** kapsamına girer

# Soru 2

[7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

**Aşama 1:** Verilen dizideki en küçük değer olan 2 sayısını buluruz. Bu sayıyı dizinin ilk indeksinde bulunan 7 sayısı ile yer değiştiririz.
    [7,3,5,8,2,9,4,15,6] &rarr; [2,3,5,8,7,9,4,15,6]

**Aşama 2:** Aşama 1'de elde edilen yeni dizi baz alınır ve ilk indeksten sonra gelen sayılardan en küçüğü olan 3 sayısını buluruz. Bu sayıyı dizinin ikinci indeksinde bulunan 3 sayısı ile yer değiştirmemiz gerekmektedir.Ama 3 sayısı hali hazırda ikinci indekste bulunduğu için dizide herhangi bir değişiklik olmayacaktır.
    [2,3,5,8,7,9,4,15,6] &rarr; [2,3,5,8,7,9,4,15,6]

**Aşama 3:** Aşama 2'de elde edilen yeni dizi baz alınır ve ikinci indeksten sonra gelen sayılardan en küçüğü olan 4 sayısını buluruz. Bu sayıyı dizinin üçüncü indeksinde bulunan 5 sayısı ile yer değiştiririz.
   [2,3,5,8,7,9,4,15,6] &rarr; [2,3,4,8,7,9,5,15,6]

**Aşama 4:** Aşama 3'de elde edilen yeni dizi baz alınır ve üçüncü indeksten sonra gelen sayılardan en küçüğü olan 5 sayısını buluruz. Bu sayıyı dizinin dördüncü indeksinde bulunan 8 sayısı ile yer değiştiririz.
   [2,3,4,8,7,9,5,15,6] &rarr; [2,3,4,5,7,9,8,15,6]