## Welcome to GitHub Pages


### Docker repository

https://hub.docker.com/u/razerisback

### Sum-of-two
```
"""
  Автор: Котосов Сергей, группа №4255
  Ссылка на сайт-портфолио: https://razerisback.github.io/
  
  Решение выполнено в функции find_sum()
  
"""


def find_sum(digits, target):
""" Функция'find_sum' возвращает индексы двух цифр, чья сумма равна целевому числу 'target'"""
    targetListOfIndexes = []
    i = 0
    while (i < len(digits)-1):
      if digits[i] + digits[i+1] == target:
        indexes = (i, i+1)
        targetListOfIndexes.append(indexes)
      i += 2  
    if not targetListOfIndexes:
      return 'Индексы не найдены'  
    return targetListOfIndexes   

Numbers = (3,1,4,1,5,9,2,6,5,3,5,8,9,7,9,3,2,3,8,4,7,6,7,4,4,5,9,2,9,9,8,0,6,7,9,8,2,2,6,5,3,5,4,1,5,3,5,8,9,0,6,5,3,5,3,2,3,8,4,7)

""" Test #1 """
target = 5
res1 = find_sum(Numbers, target)
print('targetSum=',target)
print('res1',res1)
assert res1 == [(2, 3), (16, 17), (42, 43), (54, 55)], 'test #1 passed'

""" Test #2 """
target = 8
res2 = find_sum(Numbers, target)
print('\ntargetSum=',target)
print('res2',res2)
assert res2 == [(6, 7), (8, 9), (30, 31), (40, 41), (44, 45), (52, 53)], 'test #2 passed'

""" Test #3 """
target = 54
res3 = find_sum(Numbers, target)
print('\ntargetSum=',target)
print('res3',res3)
assert res3 == 'Индексы не найдены' , 'test #3 passed'

""" Test #4 """
target = 34
res4 = find_sum(Numbers, target)
print('\ntargetSum=',target)
print('res4',res4)
assert res4 == 'Индексы не найдены' , 'test #4 passed'

""" Test #5 """
target = 8
res5 = find_sum(Numbers, target)
print('\ntargetSum=',target)
print('res5',res5)
assert res5 == [(6, 7), (8, 9), (40, 41), (44, 45), (52, 53)], 'test #5 failed'
```
