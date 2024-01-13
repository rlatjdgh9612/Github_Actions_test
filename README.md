# Github_Actions_workflow

### 이 내용은 현업에서 자주 사용하는 Github_Actions를 실습해보기 위한 용도로 제작되었습니다.

### 실습 내용 : Github Actions workflow 생성하기

### 날짜
- 2024.01.11(목)

### version 업데이트
- 0.10.0 ver : 기본 workflow 파이프라인 내용 정리 및 초기설정
- 0.11.0 ver : first.yml 파일 작성

### 참고사항 : Github Action 요소 종류

**workflows**
- 워크 플로우는 하나 이상의 job으로 구성되고 event에 의해 트리거될 수 있는 자동화된 프로세스이며, YAML으로 작성되고 Github Repository의 .github/workflows 폴더 아래에 저장한다. repository에는 여러 workflow를 가질 수 있으며 각 workflow는 서로 다른 작업을 수행할 수 있다.
**(워크 플로우는 다양한 job으로 구성되어 있고 병렬로 수행한다)**

**actions**
- 워크 플로우의 가장 작은 블럭으로 jobs를 만들기 위해 step 들을 연결할 수 있으며, 재사용이 가능한 컴포넌트로서 반복적인 코드의 양을 줄일 수 있고 git repository를 가져오거나 클라우드 공급자에게 인증을 설정할 수도 있다.

**events**
- 워크 플로우의 실행을 트리거하는 특정 활동이나 규칙을 말한다.

**jobs** 
- 여러 step으로 구성되고 가상 환경의 인스턴스에서 실행되며, 다른 job에 의존 관계를 가질 수 있고 독립적으로 병렬 실행도 가능하다.

**steps**
- task들의 집합으로 커맨드를 날리거나 쉘 스크립트 실행하는 것처럼 action을 실행할 수 있다.
**(또한, 개인적으로 만든 action을 작성할 수도 있고 github marketplace에 있는 공용 action을 사용도 가능하다)**

**runners**
- 워크 플로우가 트리거될 때 실행하는 서버이며, 각 runner는 1번에 1개의 job을 실행할 수 있. Github에서 호스팅해주는 Github-hosted runner와 직접 호스팅하는 Self-hosted runner로 나뉜다.
