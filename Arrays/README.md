# Arrays:
collection of variable of the same data type and fixed size "base-on index"

start by index=0 end by index= (arr.length-1)

 يعني هي عباره عن مجموعه متغيرات او قيم متخزنين جمب بعض من نفس نوع بيانات يعني ياه string او integer او.....

 وليها حجم ثابت متقدرش تزوده ولا تنقصه ساعه runtime

# Advantage
-Easy to use and create

-Direct access to element via index
# Limitations
1- Fixed size: can not grow or shrink dynamically

2-Homogeneus: All elements must be of the same type

3-Overhead in insertion,deletion,merging

## هنكلم علي اهم مميزه وهي access by index

لي هي سهله ب access by index عشان متخزنه في ذاكره بشكل contiguous memory يعني عناصرها جمب بعض في ذاكره دون فواصل

![](contiguousMemory.jpg)



```
index:     0      1     2       3
value:   [10]   [20]   [30]   [40]
address:   100   104    108    112
```
نوضح بقي لي الوصول ب index سهل لو انت عارف base address بتاع اول عنصر اللي هو 100 مثلا عندنا وعارف ان كل عناصر جمب بعض ومثلا كل int حجمه 4byte يعني عنصر اللي جمبه هيبقي عنوانه 104 ____> index=1 ----> ال address=base address+index * 4=104
نوصل لي *general equation* ال address=base_address+index*element_size 


![](access.png)

## note
arr[2] like as arr[50000] ----->O(1)

## دي هي اهم مميزه بتقدمه ال array لان عندك حاجه زي LinkedList هتعرف عشان توصل لعنصر هتضطر تعدي عليهم واحد واحد

# ندخل علي المشاكل بقي في insertion && delete

# insertion

لو عايز تضيف 40 في اخر خانه بس لازم تاكد ان في مكان
```
[10][20][30][]
```
هتضيف عادي
```
[10][20][30][40]
```
ونوع ده سهل عشان حجم زياده و في اخر ----> O(1)

```
Index:  0   1   2   3   4   5
Value: [5] [8] [3] [7] [2] [  ]
```
insert 9 in index =2 
                   
```
[5][8][9][3][7][2]
```
### steps
1-اتاكد ان size يسمح يعني في مكان زياده في اخر

2-تعمل shifting ناحيه يمين لعناصر من اول index اللي عايز تعمل فيه insert لي اخر عناصر

arr[5]=arr[4]
```
[5][8][3][7][2][2]
```
arr[4]=arr[3]
```
[5][8][3][7][7][2]
```
arr[3]=arr[2]
```
[5][8][3][3][7][2]
```
arr[2]=9
```
[5][8][9][3][7][2]
```
تلاحظ ان تلات عناصر اتحركوا عشان تضيف عنصر لذلك عمليه اضافه في array مش افضل حاجه خالص O(n)

         


