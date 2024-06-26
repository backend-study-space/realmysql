# 5.1 트랜잭션

## 5.1.1 MySQL에서의 트랜잭션

- 트랜잭션은 하나 이상의 논리적인 작업 셋에서 100% 보장되거나, 아무것도 적용되지 않아야 함을 의미한다.

## 5.1.2 주의사항

- 트랜잭션은 꼭 필요한 최소한의 코드에만 적용하는 것이 좋다. 이는 프로그램의 코드에서 트랜잭션의 범위를 최소화하라는 의미이다.

- 실제 예시
    - 데이터베이스 커넥션 생성과 동시에 트랜잭션을 시작하는 행위를 지양해야한다.
    - 메일 전송이나 FTP 파일 전송 작업, 혹은 네트워클르 통한 원격 서버 통신 등의 작업은 어떻게 해서든 DBMS 트랜잭션 내에서 제거해야한다. 이런 작업에서 장기적인 대기상태에 빠지면 웹 서버 뿐만 아니라 DBMS 서버까지 위험해질 것이다.
    - 트랜잭션의 범위는 최소화시키고, 별개의 작업이라면 트랜잭션을 분리해야한다.

