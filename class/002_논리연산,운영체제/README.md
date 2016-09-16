1. 컴퓨터의 연산

   * [부호비트 및 보수표현](http://bloger.kr/34)

     * ![](http://cfile3.uf.tistory.com/image/2247934C57148AA40D2774)
     * ![](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcQOFEb7rZxZUDYacrssJ96ylVUWinY23p3Lpmokdclw65fQ4G_mdQ)
     * ![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTYGc_h21XwDhlyUXFC2G4mtQd6bVMQ4nrdqKdsgUDFBggt7X1V)
* [MSB,Most significant Bit](http://bloger.kr/32)
   * [기본자료형 / 부호없는 정수형](http://ddanzimind.tistory.com/32)	
* [진법변환(진수변환) 정리](http://blog.naver.com/PostView.nhn?blogId=andjfrrk&logNo=20017501803)
   * [bit Mask 란?](http://blog.naver.com/PostView.nhn?blogId=skout123&logNo=50128841464)
   * & vs && 과 | vs ||과 ~ vs ! 의 사용시 주의 
2. 운영체제

   1. 운영체제 

      * 유닉스계열 : UNIX LINUX(Ubuntu,CentOS,Fedora) BSD MACOSX
      * 윈도우계열

   2. 운영체제의 기능 

      * 시스템하드웨어관리

        사용자 프로그램의 오류나 잘못된 자원사용감시 입출력 장치 등으 자원에 대한 연산과제어 관리

      * (가상)시스템 서비스 제공

        사용자에게 컴퓨터의 프로그램을 쉽고 효율적으로 실행 할수 있는 환경제공
        예를 들어 데스크탑화면..

      * 자원관리

        컴퓨터 시스템 하드웨어 및 소프트웨어 자원을 여러 사용자 간에 효율적 할당,관리보호
        CPU<-->프로그램(프로세스(실제로 실행중인 프로그램))(주기억장치내)<--프로그램(보조기억장치내)
        1. 프로세스 스케쥴링(자원관리)
           * FCFS(first come first Served
             준비 상태 큐에 도착한 순서에 따라 차례로 CPU를 할당
           * SJF (Shortest Job First)
             실행시간이 가장 짦은 프로세스에게 먼저 CPU할당
             평균 대기시간이 가장 적은 알고리즘
             실행시간이 긴 프로세스에 밀려 무한 연기상태 발생가능
           * Round Robin Scheduing
             시분할 시스템을 위해 고안된 방식
           * FCFS 기법 변형
             각 프로세스는 시간 할당량 동안만 실행
             완료되지 않으면 다음 프로세스에게 CPU를 넘겨주고 준비상태 큐의 가장 뒤로 배치
             할당된 시간이 클수록 FCFS 와 비슷, 할당시간이 작을 수록 문맥교환과 오버헤드 자주 발생 
           * Priority Based Scheduing
             프로세스마다 우선수위 부여
             우선수위가 동일한 경우 기법으로 할당
             가장 낮은 수위를 부여받은 프로세스의 무한 연기발생가능
           * Multi Queue Scheduing
             프로세스를 특정 그룹으로 분류할 수 있을 경우 그룹에 따라 각기 다른 준비단계 큐 사용
             준비상태 큐 마다 다른 스케줄링 기법 사용가능
             다른 준비상태 큐로 이동 불가
             하위단계 준비 큐에 있는 프로세스를 실행하는 도중이라도 상위 단계 준비사이에  큐에 프로세스가 들어오면 상위단계  프로세스에게 CPU 할당

        2. 주기억장치 관리
           * 단순관리
             자기의 프로세스영역이 아닌 곳에서 실행시 강제종료할 수 있다
           * 가상메모리 
             보조 기억장치를 주기억장치 처럼 활용
        3. 파일관리
           * 응용프로그램<--(파일 입/출력 요청)-->운영체제<--(파일 입/출력처리)-->보조기억장치
           * 모든것은 중간에 운영체제의 컨트롤하게 실행된다 직접적으로 보조기억장치에 접근하여 프로그램을 실행하지는 않는다
           * 파일시스템에 따라 데이타의 쓰기 읽기 등이 달라짐
             NTFS,FAT32,EXT3,HFS...
        4. 커널관리
           * Kernel(시스템의 뼈대)
           * 운영체제의 핵심
           * 운영체제의 정체성
           * 보안,자원관리,추상
           * Application<-->Kernel<-->CPU,RAM,DEVICE​
