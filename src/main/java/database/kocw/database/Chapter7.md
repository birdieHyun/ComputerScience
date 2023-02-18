# 7장. 관계 데이터 연산 
## 관계 데이터 연산의 개념 
## 관계 대수   

---  
<img width="443" alt="스크린샷 2023-02-17 오후 5 12 30" src="https://user-images.githubusercontent.com/115435784/219589011-8c08a2b3-d0ed-446a-bf38-4ce8725f52d3.png">
  
- 관계 데이터 연산의 개념과 종류를 알아본다. 
- 일반 집합 연산자와 순수 관계 연산자의 차이를 이해한다. 
- 일반 집합 연산자와 순수 관계 연산자를 이용해 질의를 표현하는 방법을 익힌다.  
   
  
---  
  
### 관계 데이터 연산의 개념과 종류를 알아본다.  
- **데이터 모델 = 데이터 구조 + 연산 + 제약조건**  

<img width="541" alt="스크린샷 2023-02-17 오후 5 15 03" src="https://user-images.githubusercontent.com/115435784/219589548-eac43222-8aff-4281-addf-abe1416eef0b.png">
  
- **관계 데이터 연산**  
  - 관계 데이터 모델의 연산 
  - 원하는 데이터를 얻기 위해 릴레이션에 필요한 처리 요구를 수행하는 것 
  - 관계 대수와 관계 해석이 있음 
    - 기능과 표현력 측면에서 능력이 동등함 
    - 처리 절차를 얼마나 자세히 기술하느냐에 따라 차이를 보임   

<img width="547" alt="스크린샷 2023-02-17 오후 5 16 41" src="https://user-images.githubusercontent.com/115435784/219590017-9fd0392a-eb5b-43d4-9286-bfe5e7412a9c.png">
  
- **관계 대수의 개념** 
  - 원하는 결과를 얻기 위해 릴레이션의 처리 과정을 순서대로 기술하는 언어 
    - 절차 언어 
  - 릴레이션을 처리하는 연산자들의 모임 
    - 대표 연산자 8개 
    - 일반 집합 연산자와 순수 관계 연산자로 분류됨 
  - 폐쇄 특성(closure property)이 존재함 
    - 피연산자도 릴레이션이고 연산의 결과도 릴레이션임  


<img width="525" alt="스크린샷 2023-02-17 오후 5 19 37" src="https://user-images.githubusercontent.com/115435784/219590731-e86e8fef-2645-432b-89e5-95ff656f3957.png">
  
- **일반 집합 연산자(set operation)** 
  - 릴레이션이 투플의 집합이라는 개념을 이용하는 연산자   
    <img width="570" alt="스크린샷 2023-02-17 오후 5 20 26" src="https://user-images.githubusercontent.com/115435784/219590923-05add63f-84f6-420b-9038-a511de3d5fec.png">


<img width="545" alt="스크린샷 2023-02-17 오후 5 22 56" src="https://user-images.githubusercontent.com/115435784/219591546-0c799a38-a62e-460c-a7cb-a1a227ae793f.png">
  

- **순수 관계 연산자(relation operation)** 
  - 릴레이션의 구조와 특성을 이용하는 연산자  

<img width="572" alt="스크린샷 2023-02-17 오후 5 24 28" src="https://user-images.githubusercontent.com/115435784/219591895-1f43137b-99c6-453e-a1d7-eec1d8d71b61.png">

<img width="528" alt="스크린샷 2023-02-17 오후 5 27 02" src="https://user-images.githubusercontent.com/115435784/219592485-cc4b2b7a-dde6-4637-aed4-9c8d0aab4b15.png">
  
- **일반 집합 연산자의 특성**     
  - 피연산자가 두개 필요함 
    - 두 개의 릴레이션을 대상으로 연산을 수행 
  - 합집합, 교집합, 차집합은 피연산자인 두 릴레이션이 합병이 가능해야 함 
    - 합벽 가능 조건 
      - 두 릴레이션의 차수가 같아야 함 
      - 두 릴레이션에서 서로 대응되는 속성의 도메인이 같아야 함  

<img width="552" alt="스크린샷 2023-02-17 오후 5 30 18" src="https://user-images.githubusercontent.com/115435784/219593275-1c4a1019-0a44-470c-a848-559a64e435a9.png">
  
위의 예는 나이와 직위 도메인이 동일하지 않게 때문에 합병이 불가능하다.
  
- **일반 집합 연산자 - 합집합(union)** 
  - 합병 가능한 두 릴레이션 R과 S의 합집합 :  
  - 릴레이션에 속사거나 릴레이션 S에 속하는 모든 투플로 결과 릴레이션 구성 

<img width="522" alt="스크린샷 2023-02-17 오후 5 31 43" src="https://user-images.githubusercontent.com/115435784/219593596-cd8fa099-6fdd-4ff6-9113-3754cbf4bad4.png">
    

  - 결과 릴레이션의 특성 
     - 차수는 릴레이션 R과 S의 차수와 같음 
     - 카디널리티는 릴레이션 R과 S의 카디널리티를 더한 것과 같거나 적어짐 

  - 교환적 특징이 있음  (R u S == S u R)
  - 결합적 특징이 있음  (R u S) u X  == R (S u X)


- **일반 집합 연산자 - 교집합(intersection)** 
  - 합병 가능한 두 릴레이션 R과 S의 교집합 
    - 릴레이션 R과 릴레이션 S에 속하는 모든 투플로 결과 릴레이션 구성   

<img width="519" alt="스크린샷 2023-02-17 오후 5 36 30" src="https://user-images.githubusercontent.com/115435784/219594631-f2401471-b07a-400a-8021-b009de681617.png">
   
  - 결과 릴레이션의 특성 
    - 차수는 릴레이션 R과 S의 차수와 같음 
    - 카디널리티는 릴레이션 R과 S의 어떤 카디널리티보다 크지 않음 
  - 교환적 특징이 있음 
  - 결합적 특징이 있음  
  

- **일반 집합 연산자 - 차집합(difference)**
  - 합병 가능한 두 릴레이션 R과 S의 차집합
    - 릴레이션 R에는 존재하고, 릴레이션 S에는 존재하지 않는 투플로 결과 릴레이션 구성   

<img width="538" alt="스크린샷 2023-02-17 오후 5 39 17" src="https://user-images.githubusercontent.com/115435784/219595163-e5dec7f5-877d-452b-b5b8-2c8dd0027a40.png">
  
  - 결과 릴레이션의 특성 
    - 차수는 릴레이션 R과 S의 차수와 같음 
    - R-S의 카디널리티는 릴레이션 R의 카디널리티와 같거나 적음 
    - S-R도 상동 
  - 교환적, 결합적 특징이 없음 

  
- **일반 집합 연산자 - 카티션 프로덕트(cartesian product)** 
  - 두 릴레이션 R과 S의 카티션 프로덕트 
    - 릴레이션 R에 속한 각 투플과 릴레이션 S에 속한 각 투플을 모두 연결하여 만들어진 새로운 투플로 결과 릴레이션을 구성   

<img width="383" alt="스크린샷 2023-02-17 오후 5 41 49" src="https://user-images.githubusercontent.com/115435784/219595762-f9dc3c66-92c5-4fe2-aa95-735b9dfe4fe3.png">
  
  - 결과 릴레이션의 특성 
    - 차수 릴레이션 R과 S의 차수를 더한 것과 같음 
    - 카디널리티는 릴레이션 R과 S의 카디널리티를 곱한 것과 같음 
  - 교환적 특징이 있음 
  - 결합적 특징이 있음  

  
R이 3개이고 S가 3개이면 3x3 으로 9개이다.  

- **순수 관계 연산자(relational operation)** 
  - 릴레이션의 구조와 특성을 이용하는 연산자   

<img width="1169" alt="스크린샷 2023-02-18 오전 11 17 58" src="https://user-images.githubusercontent.com/115435784/219826629-13d01ffe-26f8-4369-8774-930d4f07d7a5.png">

<img width="1154" alt="스크린샷 2023-02-18 오전 11 18 38" src="https://user-images.githubusercontent.com/115435784/219826655-1a169174-47bb-4035-a543-653088329d87.png">
  
- **순수관계 연산자 - 셀렉트(select)** 
  - 릴레이션에서 조건을 만족하는 투플만 선택하여 결과 릴레이션을 구성 
  - 하나의 릴레이션을 대상으로 연산 수행 
  - 수학적 표현법 : .... 
  - 데이터 언어적 표현법 : 릴레이션 where 조건식 
  - 조건식
    - 비교식 프레디킷(predicate)이라고도 함 
    - 속성과 상수의 비교나 속성들 간의 비교로 표현 
    - 비교연산자와 논리 연산자를 이용해 작성 

<img width="1167" alt="스크린샷 2023-02-18 오전 11 24 31" src="https://user-images.githubusercontent.com/115435784/219826888-12925987-0ac2-4dca-a13b-3ad8aa07de70.png">
  
고객 릴레이션에서 등급이 gold인 투플을 검색하시오  

<img width="1124" alt="스크린샷 2023-02-18 오전 11 25 13" src="https://user-images.githubusercontent.com/115435784/219826915-0af4d9ed-ed7f-423b-9fbd-7afe86493ae8.png">
  
위와같이 표현할 수 있는 역량을 키워야 한다.  
---
![스크린샷 2023-02-18 오전 11.25.52.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_jHnw0k%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.25.52.png)
 결과 릴레이션은 연산 대상 릴레이션의 수평적 부분 집합 
  
---  

  ![스크린샷 2023-02-18 오전 11.39.01.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_jM4Hpg%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.39.01.png)
  
---   

- **순수관계 연산자 - 셀렉트** 
  - 교환적 특징이 있다. 
  ![스크린샷 2023-02-18 오전 11.39.41.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_MoEJct%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.39.41.png)
  
  
  

- **순수관계 연산자 - 프로젝트(project)**
  - 릴레이션에서 선택한 속성의 값으로 결과 릴레이션을 구성 
  - 하나의 릴레이션을 대상으로 연산을 수행 
  - 수학적 표현법 ...(파이) 
  - 데이터 언어적 표현법 : 릴레이션 [속성리스트]  
  
![스크린샷 2023-02-18 오전 11.41.16.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_5XcNAy%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.41.16.png)

  
--- 
![스크린샷 2023-02-18 오전 11.41.50.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_fM8nrA%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.41.50.png)
  
---  
![스크린샷 2023-02-18 오전 11.42.07.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_6azDyk%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.42.07.png)
결과 릴레이션은 연산 대상 릴레이션의 수직적 부분 집합   

---  
  
- **순수 관계 연산자 - 조인(join)**  
  - 조인 속성을 이용해 두 릴레이션을 조합하여 결과 릴레이션을 구성 
    - 조인 속성의 값이 같은 투플만 연결하여 생성된 푸틀을 결과 릴레이션에 포함 
    - 조인 속성 : 두 릴레이션이 공통으로 가지고 있는 속성 
![스크린샷 2023-02-18 오전 11.44.11.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_M2e0XH%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.44.11.png)
---    

![스크린샷 2023-02-18 오전 11.44.54.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_1YWuDW%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.44.54.png)
  
조인 속성 : 고객 릴레이션의 고객 아이디, 주문 릴레이션의 주문 고객    

---  

![스크린샷 2023-02-18 오전 11.45.52.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_l4j0AS%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.45.52.png)
  
---  
  ![스크린샷 2023-02-18 오전 11.46.35.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_ANgj7z%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.46.35.png)
  
---  
- **순수관계 연산자 - 디비전(division)** 
  - 표현법 : 릴레이션1 ÷ 릴레이션2
  - 릴레이션 2의 모든 투플과 관련이 있는 릴레이션 1의 투플로 결과 릴레이션을 구성 
    - 단 릴레이션 1이 릴레이션 2의 모든 속성을 포함하고 있어야 연산이 가능하다. 
  ![스크린샷 2023-02-18 오전 11.48.15.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_CblAn8%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.48.15.png)
   
  
---    

   ![스크린샷 2023-02-18 오전 11.48.37.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_irPIU3%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.48.37.png)

등급이 사라지고, 등급을 포함한 릴레이션만 살아남는다.  
    
---    

![스크린샷 2023-02-18 오전 11.49.24.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_3SrINp%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.49.24.png)
  
  

---  

![스크린샷 2023-02-18 오전 11.50.32.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_O3y5Wg%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.50.32.png)
  
    

---  

![스크린샷 2023-02-18 오전 11.51.48.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_W7Efz3%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.51.48.png)
  
---    

  ![스크린샷 2023-02-18 오전 11.54.53.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_6NMugI%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.54.53.png)
  
---  
  ![스크린샷 2023-02-18 오전 11.56.24.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_FPRNzA%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.56.24.png)
    
  
---  
  ![스크린샷 2023-02-18 오전 11.57.20.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F_f%2F6ls2lhr942q9p0gtlpc_hh640000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_lUbOy5%2F%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202023-02-18%20%EC%98%A4%EC%A0%84%2011.57.20.png)
    
  
---  
  
  

