## Hi there 👋

클라우드 엔지니어링 3대미녀가 있었는뎁쇼<br>
김옥빈, 박은빈, 고아라 레츠고!<br>
고아라는 떠나가고 이성미가 새로 합류했답니다.<br>
(히든 멤버에는 수의 고모가 계셔요)

## 깃 컨벤션
- `Feat` : 새로운 기능 추가했을 때 사용해요.
- `Fix` : 버그 수정 시 사용해요.
- `Docs` : 문서를 수정 했을 때 사용해요.
- `Style` : 코드 포맷팅, 세미 콜론 누락에 따른 세미 콜론 추가 등의 코드의 변경이 없는 경우에 사용해요.
- `Refactor` :코드 리팩토링 시 사용해요
- `Test` : 테스트 코드 추가 시, 코드 리팩토링 후 테스트 코드 추가가 있을 때 사용해요.
- `Chore` : 빌드 업무 수정, 패키지 매니저 수정 등과 같이 코드와 관련 없는 부분을 수정했을 때 사용해요.
    - ex) `.gitignore`, `build.gradle`
- `Comment` : 주석 추가 및 변경 시에 사용해요
- `Remove` : 파일이나 폴더를 삭제할 때 사용해요.
- `Rename` : 파일 수정이나 폴더명 수정 시 사용해요.

## 브랜치 컨벤션
### **feature branch**
기능 개발을 할 때 사용하는 브랜치예요.
이는 기본적으로 공유하지 않아도 되기 때문에 본인의 로컬 저장소에서 관리해요.
- `feature/...` 형식
  
### **3. release branch**
이번 출시 버전을 준비하는 브랜치예요.
배포를 위한 전용 브랜치로 해당 브랜치를 사용하면 다음 배포를 위한 기능 개발이 계속해서 가능해요. 
- `release/...`
  
### **4. hotfix branch**
출시 버전에서 발생한 버거를 수정하는 브랜치예요.
- `hotfix/...`
# imyeomsu
##  Imyeomsu - Lck X 우리은행 
클라우드 환경에서 고가용성 고려한 탄력적 서비스를 위한 LCK X 우리은행 ImYeomSu 팀의 서비스 입니다.

---
# 아키텍처
## 애플리케이션 아키텍처
![image](https://github.com/I-m-YeomSu/imyeomsu-lck/assets/81970382/1625c015-3eab-4c6a-97c5-b7932ef1678d)


## 시스템 아키텍처
![image](https://github.com/I-m-YeomSu/imyeomsu-lck/assets/81970382/0bed8ca7-52c9-4991-8ed7-3fe22dbd5afd)


---
# 서비스 설명
## 사용 기술 스택
### 프론트 엔드
html
css
javascript
bootstrap
jquery
thymeleaf

### 백엔드
spring boot
spring security
spring data jpa
queryDsl


### 형상 관리
git
github

### 데이터베이스
Mysql
Redis

### 테스트
junit5
mockito
jacoco
coverrals

### 로그
logstash
logback
slf4j

### 기타 
jitpack


## 인증/인가
- 세션을 이용한 사용자 로그인 유지
- 분산 환경에서 서버가 여러대인 경우를 고려한 세션 스토리지 도입
- 세션 스토리지로 Redis 사용

### session storage redis
- 

## 배치

## 크롤링 

## 트러블 슈팅
### 1. 동시성 이슈 해결 
- [우리는 왜 레디스를 도입해서 분산 환경에서의 동시성 이슈를 해결했을까?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/83)
- [싱글 쓰레드인 레디스를 이용한 동시성 이슈 해결 방법](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/84)

----

# 인프라 설명
## 우리는 왜 EKS를 선택했을까?

---
# 배포
## CI/CD 플로우

## 배포 플로우

---
# 로그와 모니터링
## 로그 모니터링 플로우

---
# 트러블 슈팅


## 대용량 트래픽 해결

## 테스트 커버리지


### 테스트 커버리지 80%를 목표로 합니다.

