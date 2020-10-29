# 201028
### 파이썬 코딩테스트

완주하지 못한 선수

문제 링크: https://programmers.co.kr/learn/courses/30/lessons/42576

#### 내 답
```python
def solution(participant, completion):
    answer = ''
    participant = sorted(participant)
    completion = sorted(completion)
    for i in range(len(completion)):
        if participant[i] == completion[i]:
            continue
        else:
            answer = participant[i]
            break
    if answer == '':
        answer = participant[-1]
    return answer
```

더 좋은 방법이 없을까 하다가 **zip()** 발견.

### zip() 기능
```python
zip(*iterable): 동일한 개수로 이루어진 자료형을 묶어 주는 역할을 하는 함수.
Number = [1, 2, 3]
Name = ['Kim', 'Min', 'Chae']
Number_Name = list(zip(Number, name))
print(Number_Name)

result : [(1 ,'Kim'), (2 ,'Min'), (3 ,'Chae')]
```

개선된 코드
```python
def solution(participant, completion):

    participant.sort()
    completion.sort()

    for par, com in zip(participant, completion) :
        if par != com :
            return par

    return participant[-1] 
    ```