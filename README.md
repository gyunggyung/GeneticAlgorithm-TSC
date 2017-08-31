# GeneticAlgorithm-TSC
유전 알고리즘을 이용한 열차속도 최적화

## 유전 알고리즘이란?
유전 알고리즘(Genetic Algorithm)은 자연세계의 진화과정에 기초한 계산 모델로 최적화 문제를 찾는 기법 중 하나입니다. 생물의 진화를 모방한 진화 연산의 대표적인 기법으로, 쉽게 생각하면 가능한 좋은 해를 재생산하여 더 좋은 해를 찾는 방법입니다.  
실제 진화의 과정에서 많은 부분을 이용하며, 변이(돌연변이), 교배 연산 등을 이용합니다. 또한 세대, 인구 등의 용어도 문제 풀이 과정에서 사용됩니다.  
>[유전 알고리즘 위키백과](https://ko.wikipedia.org/wiki/%EC%9C%A0%EC%A0%84_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)

## 무엇을 할 건가?
공항철도의 최적의 운행 시간을 찾기.  
하루의 달리는 열차(약 100개)의 모든 구간(11개 구간)의 속도를 구하기

## 어떻게 만들건가?
1. 기존 속도에 0과 1로 이루어진 속도 리스트를 더합니다. (01로 이루어진 리스트를 디코딩하여 10진수로 바꿈니다.)

2. 변한 속도가 얼마나 효율적인지  ScoreFunction로 점수를 구합니다.  

3. 해집단의 상위 save_value값과 roulettes함수(룰렛휠)통해 구한 값을 더해 Selected_list_in_roulette 리스트를 만듭니다.

4. Selected_list_in_roulette리스트안에 해집단을 교배 시켜 새로운 속도 리스트를 구합니다.

5. largest_generation만큼 1~4번을 반복합니다.

### 1~2 ScoreFunction
속도가 효율적일 수록 점수가 높아집니다.

### 3 Selected_list_in_roulette 만들기

#### 상위 save_value값 구하기
ScoreFunction로 구한 점수를 sorted하여 상위 save_value(5,7~~)값을 잘라냅니다.  
가장 우수한 해들은 보존합니다.

#### roulettes함수(룰렛휠)통해 값 구하기

##### 룰렛휠이란? 
좋은 해가 높은 확률로 선택되고 나쁜 해도 선택될 확률을 주어 다양성을 높이는 방법입니다.  

```
ScoreFunction 통해 구한 점수 

```



