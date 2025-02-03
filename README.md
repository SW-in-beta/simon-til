# til-template

## 오늘 내가 배운 것들(Today I Learned)

### [2월 첫째주, 1주차]

24.02.03 Tail Recursion(Wikipedia https://en.wikipedia.org/wiki/Tail_call)
- 마지막으로 return 되는 값이 subroutine의 결과여야만 Tail Recursion
 - ex) return fibonacci(n-1) * n -> 마지막으로 수행되는 연산이 *니까 Tail Recursion이 아니다.
- 왜 사용하느냐? -> Recursion을 사용하면 호출을 할 때 마다 스택 메모리에 쌓이므로 메모리 소비가 심하다.
- Tail Call은 그걸 어떻게 해결해? -> Tail Call을 한다면, 새로운 스택 메모리를 할당하는 것이 아니라 기존 스택 메모리에 arguments만 대체하는 방식으로 호출한다. -> 메모리 낭비를 막을 수 있다.
- 그치만 CPython에서는 이런 방식을 지원하지 않는다.............. -> 스택 트레이싱을 통한 debugging을 힘들게 한다는 귀도의 생각 -> 파이썬에서는 반복문을 쓰는 것을 추천한다.
- 주로 함수형 언어에서 선호한다.
