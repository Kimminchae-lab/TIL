# 201028
### 파이썬 코딩테스트

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
