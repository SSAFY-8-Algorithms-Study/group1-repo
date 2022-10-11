## 9주차 회의록 

:calendar: : 9 PM, 22.09.27(TUE)

### :loudspeaker: 공지사항

### :heavy_check_mark: 개인 별 미션 달성도 :x:
|Problem No.|2579|17086|2805|2660|18428|
|:-----------:|:-----:|:----:|:----:|:----:|:----:|
|최현인|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|김승희|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|백자민|:heavy_check_mark:|:heavy_check_mark:|:x:|:heavy_check_mark:|:heavy_check_mark:|
|한재욱|:x:|:heavy_check_mark:|:x:|:heavy_check_mark:|:heavy_check_mark:|

### :bookmark_tabs: 코드 리뷰

#### 2579 계단 오르기

- 코드 리뷰 : 최현인
  - 핵심 기법 : DP
  - 풀이 방법 
    - dp의 점화식을 세워 보면
    - di 는 i 번째 까지 계단 점수합의 최대 값
    - d1 = n1; d2 = n1+n2, d3 = max(n1+n3, n2+n3), d4 부터는 di = max(d(i-3) + n(i-1) + ni, d(i-2) + ni) 로 세워진다
    - 세워진 점화식에 맞게 구현하면 끝


#### 17086 아기 상어 2

- 코드 리뷰 : 김승희
  - 핵심 기법 : 수학
  - 풀이 방법 
    - 처음에 들어오는 아기 상어의 위치를 큐에 넣어준다.
    - 큐의 크기만큼 for문을 돌려서 -> 아기 상어들과 특정 거리만큼 떨어진 공간을 볼 수 있다.
    - 큐에 들어있는 위치들에서 다음에 갈 수 있는 공간을 찾아 큐에 넣는다.
    - 입력으로 들어오는 map을 유지할 필요가 없기 때문에 방문한 공간을 1로 만들어 방문 체크를 한다.


#### 2805 나무 자르기

- 코드 리뷰 : 백자민
  - 핵심 기법 : 매개 변수 탐색
  - 풀이 방법
    - 0부터 나무 높이의 최댓값 사이의 값들을 이분탐색하면서 최대 자를 수 있는 높이를 구한다.

#### 2660 회장 뽑기

- 코드 리뷰 : 한재욱
  - 핵심 기법 : 그래프 탐색
  - 풀이 방법 
    - 인접리스트 그래프 문제로 품.
    - bfs탐색으로 가장 먼곳에 있는 것의 값이 회장후보의 점수라고 생각하고 그 값을 우선순위 큐에 담음
    - 우선순위 큐에 담고 그 값을 꺼내서 가장 큰 회장후보의 점수와 같은 것을 리스트에 담고
    - 리스트의 사이즈(회장 후보의 수)와 최대 점수를 답으로 출력.

#### 18428 감시 피하기

- 코드 리뷰 : 김승희
  - 핵심 기법 : 조합, 구현
  - 풀이 방법 
    - 장애물의 위치 3개를 조합으로 구한다.
    - 입력으로 들어온 origin을 복사한 후 해당 위치에 대해 장애물을 설치한다.
    - 델타 탐색을 응용하여 선생님이 감시를 시작한다.
    - 이때 while문을 도는데 범위를 벗어나거나 장애물을 만나면 while문을 빠져나온다
    - 만약 학생을 만난다면, 선생님의 감시에 걸린 것이기 때문에 더 이상 함수를 진행할 필요가 없다.
    - 선생님의 감시를 모두 피했다면 answer를 true로 만들어서 다음 프로세스를 더 이상 진행하지 않도록 처리한다. 


### :raising_hand_man: 건의 사항 :raising_hand:
