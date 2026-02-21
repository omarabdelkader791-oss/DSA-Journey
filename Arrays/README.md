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


![]()
