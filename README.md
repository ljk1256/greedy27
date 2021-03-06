# Job Scheduling 과제 

TEAM : Greedy 27 

팀원 : 임나정,박종수,이재권
---
**1. 작업 스케줄링 알고리즘이란 ?**

![과제 결](https://user-images.githubusercontent.com/80773617/114479532-b181a800-9c3b-11eb-9e31-0c1545cc0370.PNG)

* 작업의 수행 시간이 중복되지 않도록 모든 작업을 가장 적은 수의 기계에 배정하는 문제이다.
* 그리디 알고리즘(Greedy algorithm)으로 최적해를 구하는 알고리즘이다.
* 시간복잡도는 O(nlogn)+O(mn)으로 표현 할 수 있다.  
* 비지니스 프로세싱, 공장 생산 공정, 강의실/세미나룸 배정 등에 활용된다.

**2. 작업스케줄링 순서**
###### (a). 시작시간을 기준으로 작업들을 오름차순으로 정렬
###### (b). 가장 이른 시작시간을 가진 작업을 가져온다.
###### (c). 수행 시간이 중복되지 않게 수행할 기계를 찾아 배정한다.
###### (d). 배정할 수 없는 경우애는 새로운 기계에 배정
###### (e). 배정한 작업을 리스트에서 제거
###### =====>n만큼 반복 ( 모든 작업이 다 배정될 때까지 수행 )


**3. 문제**
```java
입력 : n개의 작업 t1, t2 , .., 
출력 : 각 기계에 배정된 작업 순서
시작시간의 오름차순으로 정렬한 작업 리스트를 L이라고 한다.
while(L≠Φ){
	L에서 가장 이른 시작시간을 가진 작업 t_i를 가져온다.
	if(t_i를 수행할 기계가 있으면)
		t_i를 수행할 수 있는 기게에 배정한다.
	else
		새로운 기계에 t_i를 배정한다.
	t_i를 L에서 제거한다.
}
return 각 기계에 배정된 작업 순서 
```

**4. 잡스케줄링 코드 job scheduling code**

* 클릭해 [코드]를 확인해주세요!



**5. 역할 분담**
* `main(), allocating()` : 빠른 시작시간 작업을 우선으로 중복되지않게 작업 배정해주기 _ 이재권, 임나정
* `Readme.md` : 정리 및 분석 _ 박종수


**6. 결과**


![jobscheduling 과제 결과](https://user-images.githubusercontent.com/80773617/114476462-387f5200-9c35-11eb-8998-966e38007a65.png)

[코드]: https://github.com/dlask913/Greedy27/blob/main/Job_Scheduling/src/JobSch_2.java

