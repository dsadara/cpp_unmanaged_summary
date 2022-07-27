# Section14 표준 템플릿 라이브러리(STL, Standard Template Library)

## STL Container란?

STL 컨테이너는 리스트(list) 딕셔너리(Dictionary)와 같이 어떤 요소들을 담을 수 있고  
이것들의 삽입, 삭제, 순회 등을 편하게 수행할 수 있는 라이브러리 입니다.

### STL 컨테이너 종류는 아래와 같습니다.

- 벡터(vector)
- 맵(map)
- 셋(set)
- 스택(stack)
- 큐(queue)
- 리스트(list)
- 덱(deque)

### STL 컨테이너의 특징은

1. [**템플릿 기반**]()으로 되어 있어 기본 데이터, 객체, 포인터 모두 원소로 사용할 수 있습니다.
2. **모든 컨테이너에 적용되는 표준 인터페이스**가 있습니다.
3. **메모리를 자동으로 관리** 해줍니다.

2번을 예를 들면 보통 Stack의 삽입은 Pop(), Queue의 삽입은 Enqueue()로 자료구조마다 함수명이 다릅니다. 하지만 STL 컨테이너는 Stack과 Queue 그리고 다른 자료구조들 모두 삽입을 push_back()으로 통일했습니다. 이는 함수명이 통일 되어 좋아 보이지만 단점도 있습니다. 단점은 [이 링크]()를 참고하시면 됩니다.

3번은 컨테이너의 용량이 차면 메모리를 자동으로 늘려준다는 것입니다.
new로 만드는 동적 할당 배열은 생성 시 크기를 정해줘야 했었습니다. STL 컨테이너는 생성 시 **크기를 정해주지 않아도 됩니다.**

### 크기를 정해주지 않아도 되는 이유가 뭘까요?

STL 컨테이너 vector를 생성하면 처음에 32개의 공간을 자동으로 할당해 준다고 합시다. (컴파일러마다 구현이 다를 수 있습니다)  
원소가 32개보다 많아지면 64개로 늘려주고 이보다 더 많아지면 128개로 늘려줍니다.
즉, 용량을 초과할 때 마다 용량을 2배씩 늘려줍니다.
이 과정에서 STL 컨테이너가 알아서 동적 메모리를 새로 할당하고 삭제를 해야합니다.
이때 시간이 많이 걸릴 수 있고, 메모리 단편화가 일어날 수 있습니다.

STL 컨테이너 내부에서 어떤 식으로 작동하는지는 [이 링크]()를 참고하시면 됩니다.