# 8장 데이터베이스 언어 SQL 
## 학습 목표 
![스크린샷 2023-02-19 오전 11.21.48.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Jvflrc%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.21.48.png)

- SQL의 역할을 이해하고, 이를 기능별로 분류한다. 
- SQL의 데이터 정의 기능을 예제를 통해 익힌다. 
- SQL의 데이터 조작 기능을 예제를 통해 익힌다. 

## SQL의 소개 
- **SQL (Structured Query Language)** 
  - 관계 데이터베이스를 위한 표준 질의어 
  - 1974년에 IBM 연구소에서 데이터베이스 시스템, '시스템R'을 질의하기 위해서 만들어진 구조화된 언어 
  - 미국 표준 연구소인 ANSI와 국제 표준화 기구인 ISO에서 표준화 작업을 진행 
    - 1999년 SQL-99 (SQL3)까지 표준화 작업이 완료된 후 계속 수정 및 보완되고 있음 
  
![스크린샷 2023-02-19 오전 11.24.24.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_AZmOZR%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.24.24.png)
  
![스크린샷 2023-02-19 오전 11.25.33.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_uXqeY8%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.25.33.png)
  
- **SQL의 분류** 
  - 데이터 정의어 (DDL; Data Definition Language) 
    - 테이블을 생성하고 변경 제거하는 기능을 제공   
    

  - 데이터 조작어 (DML; Data Mnipulation Language)
    - 테이블에 새 데이터를 삽입하거나, 테이블에 저장된 데이터를 수정 삭제 검색하는 기능을 제공   
    
  
  - 데이터 제어어 (DCL)
    - 보안을 위해 데이터에 대한 접근 및 사용 권한을 사용자별로 부여하거나 취소하는 기능을 제공   
  
![스크린샷 2023-02-19 오전 11.28.09.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_NkVRCI%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.28.09.png)

![스크린샷 2023-02-19 오전 11.29.28.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_F0bOAB%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.29.28.png)
    
![스크린샷 2023-02-19 오전 11.30.19.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_QYi8ba%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.30.19.png)

![스크린샷 2023-02-19 오전 11.29.55.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_z44nLT%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.29.55.png)


## SQL을 이용한 데이터 정의 
- **SQL의 데이터 정의 기능** 
  - 테이블을 생성 변경 제거  
  
![스크린샷 2023-02-19 오전 11.34.36.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_yjdMPu%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.34.36.png)
     
- 테이블 생성 : CREATE TABLE 문 
![스크린샷 2023-02-19 오전 11.35.25.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_7eWg12%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.35.25.png)

  - 1: 테이블을 구성하는 각 속성의 이름, 데이터타입, 기본 제약 사항 정의 
  - 2: 기본키 정의 
  - 3: 대체키 정의 (Microsoft Access SQL로 작동하지 않음, 강의에서는 스킵)
  - 4: 외래키 정의 
  - 5: 데이터 무결성을 위한 제약조건 정의  (Microsoft Access SQL로 작동하지 않음, 강의에서는 스킵)  
  
  - 속성의 정의 
    - 테이블을 구성하는 각 속성의 데이터 타입을 선택한 다음 널 값 허용 여부와 기본값 필요 여부를 결정 
    - NOT NULL 
      - 속성이 널 값을 허용하지 않음을 의미하는 키워드 
      - 예) 고객 아이디 VARCHAR(20) NOT NULL
    - DEFAULT (Microsoft Access SQL로 작동하지 않음)
      - 속성의 기본 값을 지정하는 키워드 
      - 예) 적립금 INT DEFAULT 0 
      - 예) 담장자 VARCHAR(10) DEFAULT '방경아'  
    

  - 키의 정의 
    - PRIMARY KEY 
      - 기본키를 지정하는 키워드 
      - 예) PRIMARY KEY(고객 아이디)
      - 예) PRIMARY KEY(주문 고객, 주문 제품 )
    - UNIQUE (Microsoft Access SQL로 작동하지 않음)
      - 대체키를 지정하는 키워드 
      - 대체키로 지정되는 속성의 값은 유일성을 가지며, 기본키와 달리 널 값이 허용됨 
      - 예) UNIQUE(고객 이름) 
  
  - 키의 정의 
    - FOREIGN KEY 
      - 외래키를 지정하는 키워드 
      - 외래키가 어떤 테이블의 무슨 속성을 참조하는지 REFERENCES 키워드 다음에 제시 
      - 예) FOREIGN KEY(소속 부서) REFERENCES 부서(부서번호)  
  
    
  - 데이터 무결성 제약조건의 정의 
    - CHECK (Microsoft Access SQL로 작동하지 않음)
      - 테이블에 정확하고 유효한 데이터를 유지하기 위해 특정 속성에 대한 제약조건을 지정 
      - CONSTRAINT 키워드와 함께 고유의 이름을 부여할 수도 있음 
      - 예) CHECK (재고량>=0 AND 재고량 <= 10000)
      - 예) CONSTRAINT CHK_CPY CHECK(제조업체 = '한빛제과')    
      
  
      
  ---
- **고객 테이블 생성을 위한 CREATE TABLE 문 작성 예** 
![스크린샷 2023-02-19 오전 11.51.07.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_yHtda7%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.51.07.png)
    
CREATE TABLE 고객(  
고객 아이디 VARCHAR(20) NOT NULL,  
고객 이름  VARCHAR(10) NOT NULL,  
나이 INT,  
등급 VARCHAR(10)NOT NULL,  
직업 VARCHAR(10),  
적립금 INT DEFAULT 0,  
PRIMARY KEY (고객 아이디)  
);  

![스크린샷 2023-02-19 오전 11.54.52.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_bNInyI%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.54.52.png)
   
---  
![스크린샷 2023-02-19 오전 11.55.52.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_pF4zvg%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.55.52.png)
CREATE TABLE 제품 (  
제품번호 VARCHAR(3) NOT NULL,  
제품명 VARCHAR(20),   
재고량 INT,   
단가 INT,   
제조업체 VARCHAR(20),  
PRIMARY KEY(제품번호),  
CHECK(재고량 >= 0 AND 재고량 <= 10000)  
);

![스크린샷 2023-02-19 오전 11.59.31.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Qpe1YX%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%EC%A0%84%2011.59.31.png)

---    

![스크린샷 2023-02-19 오후 12.00.39.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_hrcYXr%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.00.39.png)

  
CREATE TABLE 주문 (  
주문번호 INT NOT NULL,  
주문고객 VARCHAR(20),  
수량 INT,  
배송지 VARCHAR(20),  
주문일자 DATETIME,
PRIMARY KEY (주문번호),
FOREIGN KEY(주문고객) REFERENCE 고객(고객 아이디),  
FOREIGN KEY(주문제품) REFERENCE 제품(제품번호)
);

![스크린샷 2023-02-19 오후 12.06.59.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YNfjwU%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.06.59.png)
  
VARCHAR 은 가변 길이 () 안의 수가 최대 길이  
CHAR(3) 은 fix된 3글자  

---  
- **테이블 변경 : ALTER TABLE 문** 
  - 새로운 속성 추가   
  ![스크린샷 2023-02-19 오후 12.09.54.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_5m4FeH%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.09.54.png)
    
ALTER TABLE 고객 ADD 가입날짜 DATETIME;
  
  - 기존 속성 삭제  
![스크린샷 2023-02-19 오후 12.11.56.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_xyKZrs%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.11.56.png)
    - CASCADE 
      - 삭제할 속성과 관련된 제약조건이나 참조하는 다른 속성을 함께 삭제 
    - RESTRICT 
      - 삭제할 속성과 관련된 제약조건이나 참조하는 다른 속성이 존재하면 삭제 거부   
  
![스크린샷 2023-02-19 오후 12.12.51.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_akMfLd%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.12.51.png)
  
ALERT TABLE 고객 DROP 등급 CASCADE;  
![스크린샷 2023-02-19 오후 12.16.26.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_ocP0VA%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.16.26.png)
    
  
- **테이블 제거 : DROP TABLE문**  
![스크린샷 2023-02-19 오후 12.17.32.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_QrZE6p%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.17.32.png)
  - CASCADE 
    - 제거할 테이블을 참조하는 다른 테이블도 함께 제거 
  - RESTRICT 
    - 제거할 테이블을 참조하는 다른 테이블이 존재하면 제거 거부 
  
![스크린샷 2023-02-19 오후 12.17.43.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_mzs8St%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.17.43.png)
DROP TABLE 고객 RESTRICT;  
![스크린샷 2023-02-19 오후 12.19.32.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_0G9cf5%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.19.32.png)
  

## SQL을 이용한 데이터 조작     

- **ㄴSQL의 데이터 조작 기능** 
  - 데이터 검색, 새로운 데이터 삽입, 데이터 수정, 데이터 삭제  
  ![스크린샷 2023-02-19 오후 12.20.22.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_vLCtD6%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.20.22.png)  

- **데이터 검색 : SELECT 문** 
  - 기본 검색 
  - **SELECT 키워드와 함께 검색하고 싶은 속성의 이름 나열** 
  - **FROM 키워드와 함꼐 검색하고 싶은 속성이 있는 테이블의 이름 나열** 
  - 검색 결과는 테이블 형태로 반환된다.  
  ![스크린샷 2023-02-19 오후 12.21.55.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Cd3IDX%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.21.55.png)
  
  - ALL
    - 결과 테이블이 투플의 중복을 허용하도록 지정, 생략 가능 (Microsoft Access default 값) 
  - DISTINCT
    - 결과 테이블이 투플의 중복을 허용하지 않도록 지정   
    
  - 기본 검색   
![스크린샷 2023-02-19 오후 12.25.20.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_0QKUVg%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.25.20.png)
    
SELECT 고객아이디, 고객이름, 등급  
FROM 고객;
  
![스크린샷 2023-02-19 오후 12.26.28.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_O0CGgT%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.26.28.png)

  
![스크린샷 2023-02-19 오후 12.26.55.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_RdYTr5%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.26.55.png)

  
SELECT 고객 아이디, 이름, 나이, 등급, 직업, 적립금  
FROM 고객;  
![스크린샷 2023-02-19 오후 12.27.44.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_edswoK%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.27.44.png)
  
위를 간략히 하면  
SELECT *  
FROM 고객;  
-> 모든 속성을 검색할 땐, 속성의 이름을 나열하지 않고 * 로 표시할 수 있다.   
  
![스크린샷 2023-02-19 오후 12.28.48.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Pf4Zd7%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.28.48.png)

  
SELECT 제조업체   
FROM 제품;  
![스크린샷 2023-02-19 오후 12.29.30.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_piT9r1%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.29.30.png)
(ALL을 사용하면 같은 값이 나온다.)
  
중복 제거 위해   
SELECT 제조업체 DISTINCT  
FROM 제품;  
    ![스크린샷 2023-02-19 오후 12.30.59.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_JwtzeF%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.30.59.png)
  
  - AS 키워드를 이용해 결과 테이블에서 속성의 이름을 바꾸어 출력 가능  

![스크린샷 2023-02-19 오후 12.31.45.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_sRFYwr%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.31.45.png)
  
SELECT  제품명, 단가 AS 가격
FROM 제품;  
![스크린샷 2023-02-19 오후 12.32.40.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_7wy7rm%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.32.40.png)

  
  - **(2) 산술식을 이용한 검색**  
    - SELECT 키워드와 함께 산술식 제시  
      - 산술식 : 속성의 이름과 +-*/ 등의 산술 연산자와 상수로 구성 
    - 속성의 값이 실제로 변경되는 것은 아니고, 결과 테이블에서만 계산된 결과 값이 출력된다.  
    
![스크린샷 2023-02-19 오후 12.46.54.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_kTpjJw%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.46.54.png)
  
SELECT 제품명, 단가 + 500 AS 조정단가  
FROM 제품;  
  ![스크린샷 2023-02-19 오후 12.48.20.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_SEqVIQ%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.48.20.png)
  
  - **(3) 조건 검색** 
    - 조건을 만족하는 데이터만 검색  
  ![스크린샷 2023-02-19 오후 12.49.07.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_dd1QIa%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.49.07.png)
    
    - **WHERE 키워드와 함께 비교 연산자와 논리 연산자를 이용한 검색 조건 제시**  
    - 숫자 뿐만 아니라, 문자나 날짜 값을 비교하는 것도 가능  
      - 예) 'A' < 'C'
      - 예) '2013-12-01' < '2013-12-02'  
    - 조건에서 문자나 날짜 값은 작은 따옴표로 묶어서 표현   
  
![스크린샷 2023-02-19 오후 12.51.02.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_NRr4Do%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.51.02.png)
  
다르다를 != 가 아닌 <> 로 표현   

![스크린샷 2023-02-19 오후 12.52.04.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_u11XCs%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.52.04.png)
  
SELECT 제품명, 재고량, 단가  
FROM 제품  
WHERE 제조업체 = '한빛제과';  

![스크린샷 2023-02-19 오후 12.53.27.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_P19G2N%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.53.27.png)

  

![스크린샷 2023-02-19 오후 12.54.53.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_JBRPHW%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.54.53.png)
  
SELECT 주문제품, 수량, 주문일자    
FROM 주문   
WHERE 고객이름 = 'apple' AND 수량 >= 15;  

![스크린샷 2023-02-19 오후 12.56.06.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_7DyKiz%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%2012.56.06.png)
    
![스크린샷 2023-02-19 오후 1.15.41.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_61hwxd%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%201.15.41.png)
  
  
![스크린샷 2023-02-19 오후 1.16.45.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_17lCWf%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%201.16.45.png)
  
SELECT 제품명, 단가, 제조업체  
FROM 제품   
WHERE 단가 >= 2000 AND 단가 <= 3000;  
![스크린샷 2023-02-19 오후 1.18.58.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_37Hj0S%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%201.18.58.png)
    
  
  - **(4) LIKE를 이용한 검색** 
    - LIKE 키워드를 이용해 부분적으로 일치하는 데이터를 검색 
    - 문자열을 이용하는 조건에만 LIKE 키워드 사용 가능     
    - 
  
![스크린샷 2023-02-19 오후 2.43.05.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_rWdwFY%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.43.05.png)
      

![스크린샷 2023-02-19 오후 2.46.51.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YPHOid%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.46.51.png)
    

- **고객 테이블에서 성이 김씨인 고객의 고객이름, 나이, 등급, 적립금을 검색해보자** 
  
SELECT 고객이름, 나이, 등급, 적립금  
FROM 고객  
WHERE 고객이름 LIKE '김*';  
    
![스크린샷 2023-02-19 오후 2.50.39.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_5GANtn%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.50.39.png)
  
- **고객 테이블에서 고객 아이디가 5자인 고객의 고객아이디, 고객이름, 등급을 검색해보자**  
  
SELECT 고객아이디, 고객이름, 등급  
FROM 고객 
WHERE 고객아이디 LIKE '?????';    


![스크린샷 2023-02-19 오후 2.52.36.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_kY7JkR%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.52.36.png)
  
- **(5) NULL을 이용한 검색** 
  - IS NULL 키워드를 이용해 검색 조건에서 특정 속성의 값이 널 값인지를 비교  
  - IS NOT NULL 키워드를 이용하면 특정 속성의 값이 널 값이 아닌지를 비교  
  
- **고객 테이블에서 나이가 아직 입력되지 않은 고객의 고객 이름을 검색해보자** 
    
SELECT 고객이름  
FROM 고객  
WHERE 나이 IS NULL   


![스크린샷 2023-02-19 오후 2.56.36.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_RS8kpR%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.56.36.png)
  
  
- **고객 테이블에서 나이가 이미 입력된 고객의 고객이름을 검색해보자** 
  
SELECT 고객이름  
FROM 고객  
WHERE 나이 IS NOT NULL;    
  
 
  
![스크린샷 2023-02-19 오후 2.57.49.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_TIriMb%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.57.49.png)
  
- (6) **정렬 검색**  
  - **ORDER BY 키워드를 이용해 결과 테이블 내용을 사용자가 원하는 순서로 출력** 
  - ORDER BY 키워드와 함께 정렬 기준이 되는 속성과 정렬 방식을 지정 
    - 오름차순(기본) : ASC / 내림차순 : DESC  
    - 여러 기준에 따라 정렬하려면 정렬 기준이 되는 속성을 차례대로 제시 
![스크린샷 2023-02-19 오후 2.59.21.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_HeW4ly%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%202.59.21.png)
  
- **고객 테이블에서 고객이름, 등급, 나이를 검색하되, 나이를 기준으로 내림차순 정렬해보자**  
  
SELECT 고객이름, 등급, 나이  
FROM 고객  
WHERE  
ORDERED BY 나이 DESC;
  
![스크린샷 2023-02-19 오후 3.02.37.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_8nGURe%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.02.37.png)
  
- **주문 테이블에서 수량이 10개 이상인 주문의 주문고객, 주문제품, 수량, 주문일자를 검색해보자. 단 주문제품을 기준으로 오름차순으로 정렬하고, 동일 제품은 수량을 기준으로 내림차순 정렬해보자.**  
  
SELECT 주문고객, 주문제품, 수량, 주문일자  
FROM 주문  
WHERE 수량 >= 10   
ORDERED BY 주문제품 ASC, 수량 DESC;  
  
![스크린샷 2023-02-19 오후 3.14.04.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_7U7MSl%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.14.04.png)


- **(7) 집계 함수를 이용한 검색**  
  - 특정 속성 값을 통계적으로 계산한 결과를 검색하기 위해 집계 함수를 이용 
    - 집계 함수 (aggregate function)
      - 개수, 합계, 평균, 최대값, 최소값의 계산 기능을 제공 
  - 집계 함수 사용시 주의 사항  
    - 집계 함수는 널인 속성 값은 제외하고 계산함 
    - 집계 함수는 WHERE 절에서는 사용할 수 없고 SELECT 절이나 HAVING 절에서만 사용 가능  
  
![스크린샷 2023-02-19 오후 3.17.14.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_61N2nW%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.17.14.png)
  
- **제품 테이블에서 모든 제품의 단가 평균을 검색해보자** 
  
SELECT AVG(단가)  
FROM 제품;   

![스크린샷 2023-02-19 오후 3.19.42.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_pqBhUA%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.19.42.png)
  
![스크린샷 2023-02-19 오후 3.20.06.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_U3ydXh%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.20.06.png)
  
- **한빛제과에서 제조한 제품의 재고량 합계를 제품 테이블에서 검색해보자** 
  
SELECT SUM(제품)  
FROM 제품  
WHERE 제조업체 = '한빛제과';

![스크린샷 2023-02-19 오후 3.21.58.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_lbT00p%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.21.58.png)

  
- **고객 테이블에 고객이 몇명 등록되어 있는지 검색해보자**    
어떤 속성이 NULL 값인지에 따라 검색이 달라질 수 있다. 
  
- 고객 아이디 속성을 이용해 계산하는 경우  
SELECT COUNT(고객아이디) AS 고객수  
FROM 고객;  

  
- 나이 속성을 이용해 계산하는 경우  
SELECT COUNT(나이) AS 고객수  
FROM 고객;  
  
- *를 이용해 계산하는 경우  
SELECT COUNT(*) AS 고객수  
FROM 고객;  
  
일반적으로 기본키나, * 을 이용해서 계산한다.  
  
  ![스크린샷 2023-02-19 오후 3.25.00.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_TVE1Eb%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.25.00.png)

    
- **제품 테이블에서 제조업체의 수를 검색해보자.**  
  
SELECT COUNT(DISTINCT 제조업체) AS 제조업체 수  
FROM 제품;
    
- **(8) 그룹별 검색**  
![스크린샷 2023-02-19 오후 3.27.16.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_0moMv5%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.27.16.png)
  
  - GROUP BY 키워드를 이용해 특정 속성의 값이 같은 투플을 모아 그룹을 만들고, 그룹별로 검색 
  - GROUP BY 키워드와 함꼐 그룹을 나누는 기준이 되는 속성을 지정  
  - HAVING 키워드를 함께 이용해 그룹에 대한 조건을 작성 
  - 그룹을 나누는 기준이 되는 속성을 SELECT 절에도 작성하는 것이 좋음   
  
- **주문 테이블에서 주문 제품별 수량의 합계를 검색해보자**  
  
SELECT 주문제품, SUM(수량) AS 총주문수량
FROM 주문    
GROUP BY 주문제품   

![스크린샷 2023-02-19 오후 3.34.35.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_ZVdEzz%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.34.35.png)
  
  
SELECT 제조업체, COUNT(*) AS 제품수, MAX(단가) AS 최고가  
FROM 제품  
GROUP BY 제조업체
  

![스크린샷 2023-02-19 오후 3.37.28.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_FAE9M1%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.37.28.png)
  
  
- **제품 테이블에서 제품을 3개 이상 제조한 제조업체별로 제품의 개수와, 제품 중 가장 비싼 단가를 검색해보자.**  
  
SELECT 제조업체, COUNT(*) AS 제품의 개수, MAX(단가) AS 최고가 
FROM 제품    
GROUP BY 제조업체 HAVING COUNT(*) > 3;


![스크린샷 2023-02-19 오후 3.40.27.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_cbjAPm%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-19%20%EC%98%A4%ED%9B%84%203.40.27.png)

  
- **고객 테이블에서 적립금 평균이 1000원 이상인 등급에 대해 등급별 고객 수와 적립금 평균을 검색해보자.**  
  
SELECT 등급, COUNT(*) AS 고객수, AVG(적립금) AS (평균적립금)    
FROM 고객     
WHERE  
ORDERED BY  
GROUP BY 등급 HAVING AVG(적립금) >= 1000  











