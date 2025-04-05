# x만큼 간격이 있는 n개의 숫자
- [링크](https://school.programmers.co.kr/learn/courses/30/lessons/12954?language=python3)

## 나의 풀이
```py
def solution(x, n):
    return [x * i for i in range(1, n+1)]
```

## 다른 사람의 풀이1
```py
def number_generator(x, n):
    return [i for i in range(x, x*(n+1), x)]
```
- 테스트 결과
    ```
    테스트 8 〉	실패 (런타임 에러)
    ```
    - x가 0인 경우에 대해서 에러가 발생함.

## 개선된 풀이
```py
def solution(x, n):
    if x <=0:
        return [x * i for i in range(1, n+1)]
    else:
        return list(range(x,n*x+1,x))
```
- 테스트 결과 : 성능 향상
    ```
    테스트 13 〉	통과 (0.11ms, 9.21MB) -> 통과 (0.04ms, 9.03MB)
    ```
- 코드 가독성이 하락했지만, 성능 향상
