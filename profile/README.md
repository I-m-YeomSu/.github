## Hi there 👋

클라우드 엔지니어링 3대미녀가 있었는뎁쇼<br>
김옥빈, 박은빈, 고아라 레츠고!<br>
고아라는 떠나가고 이성미가 새로 합류했답니다.<br>
(히든 멤버에는 수의 고모가 계셔요)


# Imyeomsu - Lck X 우리은행 
클라우드 환경에서 고가용성을 고려한 탄력적 서비스, LCK X 우리은행 ImYeomSu 팀의 서비스 입니다.
## ImYeomSu Server
- [ImYeomsu - Project Server](https://github.com/I-m-YeomSu/imyeomsu-lck)
- [ImYeomsu - Crawling Server](https://github.com/I-m-YeomSu/imyeomsu-crawling)
- [ImYeomsu - Batch Server](https://github.com/I-m-YeomSu/imyeomsu-batch)
- [ImYeomsu - Common Utils Server](https://github.com/I-m-YeomSu/imyeomsu-lck-common-utils)
## ImYeomSu Docs
- [임염수팀 WBS](https://docs.google.com/spreadsheets/d/1I1WK-1JCvNs0hG4PDDv7Ypw4TtAw7-VgCnqHPtyDScw/edit#gid=0)
- [임염수팀 ERD](https://www.erdcloud.com/d/bgob3mffRuqrbbxDd)


# Application
## Application Architecture
![image](https://github.com/I-m-YeomSu/imyeomsu-lck/assets/81970382/1625c015-3eab-4c6a-97c5-b7932ef1678d)

## Skills
### Front-end - 프론트엔드
<div>
    <img src="https://img.shields.io/badge/-HTML-E34F26?style=flat&logo=Html5&logoColor=white"/>
    <img src="https://img.shields.io/badge/-CSS-1572B6?style=flat&logo=CSS3&logoColor=white"/>
    <img src="https://img.shields.io/badge/-Javascript-F7DF1E?style=flat&logo=javascript&logoColor=white"/>
    <img src="https://img.shields.io/badge/-Thymeleaf-005F0F?style=flat&logo=thymeleaf&logoColor=white"/>
    <img src="https://img.shields.io/badge/-Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white"/>
    <img src="https://img.shields.io/badge/-JQuery-0769AD?style=flat&logo=JQuery&logoColor=white"/>
</div>

### Back-end - 백엔드
<div>
  <img src="https://img.shields.io/badge/-SpringBoot-6DB33F?style=flat&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Spring Security-6DB33F?style=flat&logo=springsecurity&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Spring Data Jpa-6DB33F?style=flat&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Query Dsl-4695EB?style=flat&logoColor=white"/>
</div>

### Version Control - 형상 관리
<div>
  <img src="https://img.shields.io/badge/-Git-F05032?style=flat&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/-GitHub-181717?style=flat&logo=GitHub&logoColor=white"/>
</div>

### DataBase - 데이터베이스 
<div>
  <img src="https://img.shields.io/badge/-Mysql-4479A1?style=flat&logo=MySQL&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Redis-DC382D?style=flat&logo=Redis&logoColor=white"/>
</div>

### Test - 테스트
<div>
  <img src="https://img.shields.io/badge/-Junit5-25A162?style=flat&logo=Junit5&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Mockito-41AD48?style=flat"/>
  <img src="https://img.shields.io/badge/-Jacoco-891B26?style=flat/>
  <img src="https://img.shields.io/badge/-Coverrals-173B3F?style=flat"/>
</div>

### Log - 로그
<div>
  <img src="https://img.shields.io/badge/-Logback-E1763F?style=flat"/>
  <img src="https://img.shields.io/badge/-Slf4j-189C01?style=flat" />
</div>

### ETC - 기타 
<img src="https://img.shields.io/badge/-Jitpack-33485C?style=flat"/>

### Collaboration tool - 협업 툴
<div>
  <img src="https://img.shields.io/badge/-Slack-4A154B?style=flat&logo=Slack&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Notion-000000?style=flat&logo=Notion&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Google Sheets-34A853?style=flat&logo=Google Sheets&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Google Slides-FBBC04?style=flat&logo=Google Slides&logoColor=white"/>
</div>

## Implement Details - Service 
### 1. Authentication/Authorization
- 세션을 이용한 사용자 로그인 유지
- 분산 환경에서 서버가 여러대인 경우를 고려한 세션 스토리지 도입
- 세션 스토리지로 Redis 사용

### 2. Using Redis for Session Persistence - 세션 유지를 위한 레디스 사용
- [분산 환경에서 세션 유지를 위해서 우리는 왜 redis를 선택했으며, 세션 스토리지 방식을 채택했을까?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/85)

### 3. Concurrency Problem Sorving - 동시성 문제 해결
- 기존의 싱글 스레드를 제공하는 레디스를 세션 스토리지로 사용하고 있어 추가적인 인프라 구성이 없어 이를 동시성 문제 해결에 도입하고자 했다. 그러나 이 역시 분산 환경에서는 문제가 되었고 추가적으로 분산 환경에서의 동시성 문제 해결을 위해서 레디스 분산 락을 이용해서 이를 해결했다.
- [싱글 쓰레드인 레디스를 이용한 동시성 이슈 해결 방법 - 동시성 문제 해결 (단일 서버)](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/84)
- [우리는 왜 레디스를 도입해서 분산 환경에서의 동시성 이슈를 해결했을까? - 동시성 문제 해결 (분산 서버)](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/83)

### 4. Resolving Concurrency Issues in Batch Servers - 배치 서버에서의 동시성 문제 해결
- 크롤링 후에 데이터를 레디스에서 관리하고 있다. 그러나 우리는 이를 Mysql과 같은 RDB에서 영속적으로 관리하고자 했다. 그래서 스케줄링을 걸어 해당 데이터를 주기적으로 싱크를 맞춰주고 있었는데 EKS 환경에서의 분산 환경 문제가 발생했다. 우리는 이를 해결 하기 위해서 멀티 환경에서의 스케줄 처리하기 라는 타이틀로 해결하고자 했다.
- [분산 환경에서의 배치 스케줄링 작업에서의 데이터 동시성 문제는 어떻게 해결 했을까?]()

### 5. Enhancing Code Reusability and Preventing Code Duplication by Libraryfying the Project - 프로젝트를 라이브러리화 하여 코드 중복을 방지하고 재사용성을 높힌 방법
- 개발을 진행하면서 중복된 코드가 계속해서 늘어나고 있다는 문제를 느꼈습니다. 예를 들어, 공통으로 사용되는 DTO는 클래스명만 다르게 여러 번 중복 정의되어 있는 것을 발견했고, 예외 처리 관련 기능도 중복되어 구현되고 있음을 알게 되었습니다.
- 또한 저희 팀은 테스트 커버리지를 80%로 설정하고 있었는데, 테스트 불가능한 코드가 계속해서 늘어나면서 목표에 도달하기가 어려워지고 있다는 것을 깨달았습니다.
- 이러한 문제를 인식하고, 공통으로 사용하는 코드를 자바 라이브러리로 만들어 사용할 수 있도록 작업을 진행했습니다.
- [프로젝트를 라이브러리화 하여 코드 중복을 방지하고 재사용성을 높이는 방법](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/94)

### 6. Test 
- 기능 구현 후에 더 안정적인 확인을 위해서 단위 테스트를 진행하였습니다.
- 또한 테스트 커버리지를 80프로로 잡고 진행함에 따라서 더 안정적인 서비스를 제공할 수 있다고 판단하였습니다.
- 이를 위해 우리팀은 junit5와 mockito를 사용하였고 차후에는 통합 테스트를 통해 안정성을 확인 했습니다.
#### 6-1. 테스트 커버리지 확인 작업
- 테스트 작업을 진행하며 80%라는 구체적인 지표가 목표로 제시되어 있고 이를 위해 jacoco와 coveralls를 통해 확인할 수 있게 했습니다.
- [우리팀이 테스트 작업 후에 이를 가시화 하기 위한 방법](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/95)

# Infra
## System Architecture
![image](https://github.com/I-m-YeomSu/.github/assets/81970382/58bbea37-ccc9-42f4-b2a4-f8a44dcaea15)
### 구성과 관련해서 .. 
- [외부 통신과 보안 강화를 위한 Nat Gateway와 Bastion Host](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/90)
- [7계층 통신이 필요한 웹 애플리케이션에 NLB를 사용한 이유와 우리팀의 구조적인 보안 문제 해결을 위한 서비스 아키텍처 구성에 대한 이유](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/91)
- [WAF와 CloudFront는 어떤 역할을 하고 있을까]()
## 우리는 왜 EKS를 선택했을까?
- [임염수 팀이 EKS를 선택한 이유는 무엇일까?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/87)
- [우리 팀은 도커 컴포즈 대신 K8S를 사용한 이유가 무엇일까?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/89)

## CI/CD
### 1. CI/CD Flow
![image](https://github.com/I-m-YeomSu/imyeomsu-lck/assets/81970382/0e7ff775-65fb-46d9-8f01-f8f891c05e67)

### 2. CI/CD Pipeline
- [EKS 환경에서의 CI/CD는 어떻게 진행했을까?]()

## Deploy Flow - 배포

## Log and Monitoring - 로그와 모니터링 
### 1. Application Log and Monitoring
![image](https://github.com/I-m-YeomSu/imyeomsu-lck/assets/81970382/a36c826e-8201-44f6-89b1-97b7d805e7b2)
- [우리는 어떻게 애플리케이션 레벨의 로그를 정제하고 사용했을까?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/86)

### 2. System Metric 
- [우리는 어떻게 메트릭 정보를 모니터링 했고 추후 어떻게 더 발전시켜 반영할 것인가?](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/88)

### 3. Kubernetes Monitoring Dashboard
- [쿠버네티스 대시보드 사용기](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/93)
- [쿠버네티스 대시보드와 관련된 트러블 슈팅](https://github.com/I-m-YeomSu/imyeomsu-lck/issues/92)

## 대용량 트래픽 해결

## 테스트 커버리지


### 테스트 커버리지 80%를 목표로 합니다.

## 추가적인 이야기
### 클라우드 환경에서의 고려 사항
- [인프라를 관리하는 입장에서 추가적인 인프라 구축에 관한 이야기]()

# 컨벤션과 관련해서..
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

