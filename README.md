# 기능 구현 목록

- **View**
    - 입력
       - 자동차 이름
       - 시도 횟수  
    - 출력    
       - 입력된 값이 정상: 실행 결과문 출력
       - 입력된 값이 비정상: 에러 메시지 출력   
       - 턴이 시도 횟수에 도달 한 경우: 우승자 이름 출력
    <br>
    
- **Model**
    - Input validation 메소드 구현  
       - 자동차 이름
       - 시도 횟수
    - Car 클래스 리스트를 만들어 자동차 이름을 저장하는 메소드 구현
    - 0-9사이의 랜덤한 수를 뽑아 4이상이면 차를 1칸 전진시키는 메소드를 Car 클래스에 구현
    - 전진 메소드를 이용해 매턴마다 참가 자동차들의 위치를 갱신시키는 메소드 구현
    - 우승자 판별 메소드와 우승자 리스트 생성 메소드 구현
    <br>
    
- **Controller**
    - 참가 자동차 리스트 저장
       - view에서 문자열 입력 받아 변수에 저장
       - model에서 valid한지 검증
            - valid하다면 Car 클래스 리스트에 저장
            - valid하지 않다면 view에서 exception 던지고 에러 메시지 출력 후 다시 받기
    - 시도 횟수 저장
        - view에서 문자열 입력 받아 변수에 저장
        - model에서 valid한지 검증
            - valid하다면 상수 값으로 저장
            - valid하지 않다면 view에서 exception 던지고 에러 메시지 출력 후 다시 받기
    - 게임 실행
        - model의 위치 갱신 메소드를 이용해 각 자동차의 위치를 매턴 마다 갱신
        - 1대 이상의 자동차의 위치가 goal과 같아질 경우 우승자 리스트 생성
        - view의 우승자 출력 메소드로 우승자 이름 출력
    <br>

---