# Linux Command
+ ***프로세스는 현재 컴퓨터에서 연속적으로 실행되고 있는 프로그램***을 말하며, 사용자가 입력한 명령어도 프로세스가 되어 실행된다.

+ 종종 스케줄링의 대상이 되는 작업(task)과 거의 같은 의미로 쓰인다.

***

# top (table of processes)
+ ***CPU와 메모리 이용에 관한 프로세스의 정보를 실시간으로 출력한다.***

+ 유닉스 계열 운영체제에서의 작업 관리자이다.

***

## *요약 영역과 load average*
![1](https://user-images.githubusercontent.com/104607822/171815985-f973a9dd-787b-40e2-afa3-d06dd61e84b2.png)

+ 왼쪽 위부터 ***현재 시각, 시스템이 가동된 시간, 활성 사용자 세션 수***를 의미한다.

+ load average는 ***CPU에 실행 중이거나 대기 중인 작업의 개수의 평균을 나타내는 값***이다. 앞에서부터 1분, 5분 15분의 평균값을 보여준다.

***

## *Tasks*
![2](https://user-images.githubusercontent.com/104607822/171816306-2c2eb01b-70bd-4846-8dba-0153c8627de5.png)

+ 현재 프로세스의 상태를 보여준다.
***
+ `total` : 총 프로세스의 수이다.

+ `running` : CPU에서 실행 중이거나 실행 대기열에 존재하여 실행할 준비가 되어있는 프로세스이다.

+ `sleeping` : I/O 작업이 완료되기를 기다리는 프로세스이다.

+ `stopped` : Ctrl + Z 등과 같은 제어 시그널로 종료된 프로세스이다.

+ `Zombie` : 종료되었지만 리소스를 차지하고 있는 프로세스를 의미한다.

***

## *작업 영역*
![5](https://user-images.githubusercontent.com/104607822/171816582-100c245c-45fc-47ca-a0ce-d5117848c7d0.png)

***

+ `PID` : 프로세스를 식별하는 고유한 프로세스 ID이다.

+ `USER` : 프로세스를 시작한 사용자의 이름이다.

+ `PR, NI` : 커널에 의해서 스케줄링 되는 우선순위, PR 설정에 사용하는 CPU 사용률을 의미한다.

+ `S` : 프로세스의 현재 상태를 나타낸다.

+ `TIME+` : 프로세스가 사용한 총 CPU 시간이다.

+ `COMMAND`는 프로세스의 이름을 나타낸다.

***

## *옵션*
|Key|Action|
|---|---|
|-b|배치(batch)모드에서 시작한다.|
|-n|실행주기를 설정한다.|
|shift + p|CPU 사용률을 내림차순으로 정렬한다.|
|shift + m|메모리 사용률을 내림차순으로 정렬한다.|
|k|PID를 입력하여 프로세스를 종료한다.|

***

# ps (process status)
+ ***현재 실행 중인 프로세스 목록과 상태를 보여준다.***

***

## *옵션*
|Key|Action|
|---|---|
|-A|모든 프로세스를 출력한다.|
|-e|커널 프로세스를 제외한 모든 프로세스를 출력한다.|
|-f|full format으로 출력한다.|
|-u|입력한 사용자의 프로세스를 출력한다.|
|-r|현재 실행 중인 프로세스를 출력한다.|
|-p|PID를 지정하여 출력한다.|
|-x|사용자가 로그아웃 이후 실행 중인 프로세스를 출력한다.|

***

## *$ ps -ef 출력 필드*
![11](https://user-images.githubusercontent.com/104607822/171792335-7692d96b-e669-4979-ac93-719d86dab9fa.png)

***

+ `USER` : 프로세스를 시작한 사용자의 이름이다.

+ `UID` : 사용자의 ID이다.

+ `PID` : 프로세스를 식별하는 고유한 프로세스 ID이다.

+ `PPID` : 부모 프로세스의 PID이다.

+ `C` : 프로세스의 CPU 사용량이다.

+ `STIME` : 프로세스가 실행된 시간이다.

+ `TTY` : 해당 프로세스의 제어 터미널이다.

+ `TIME` : 프로세스가 사용한 총 CPU 시간이다.

+ `CMD`: 프로세스의 이름을 나타낸다.

***
