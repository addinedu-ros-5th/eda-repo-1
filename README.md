# eda-repo-1
EDA 프로젝트 1조 저장소 2024.03.25 14:44 updated

### 초록
한국을 포함해 전세계에서 많은 사람들에게 사랑을 받고 플레이하는 온라인 팀 대전 게임 리그 오브 레전드에서 
유저들에게 실력 향상을 위한 방법으로 추천되는 방법에 대해 Riot에서 제공되는 정보를 바탕으로 통계를 내고 분석하여 이 방법들이 실제로 효과가 있는지 확인해본다.

### 데이터 수집 방법
1. Riot Dev Homepage에서 API 인증 KEY를 발급받는다.
2. 리그별 소환사(플레이어) 목록(puuid)을 요청한다.
3. puuid를 통해 플레이어의 이름과 게임 정보를 가져온다.
4. 게임 정보에서 필요한 데이터와 불필요한 데이터를 분리하고 저장한다.

### 데이터 수집 대상 선정과 이유
Riot Open API에서 일반 개발자에게 제공하는 데이터는 챌린저, 그랜드마스터, 마스터 등급이 있다. 챌린저 300명, 그랜드마스터 700명으로 표본으로 삼기에 부족한 감이 있다. 따라서 데이터 수집은 상위 등급 중 등급 내 격차를 확인할 수 있는 15000명이 있는 마스터 티어이며 상위 200명과 하위 200명을 표본으로 삼았다. 게임 기록은 라이엇에서 제공하는 최대치인 100개의 게임을 가져온다.

### 데이터 분석 방법
Riot Open API의 게임 데이터에서 제공하는 정보는 게임 일시와 고유 게임 번호 등을 갖고있으며 플레이어 데이터는 280개로 개인 기록과 도전과제를 담고있으며 팀 별 오브젝트 처치 정보를 포함하고 있다.
이 중에서 승패에 유의미한 영향을 끼칠 것으로 추측되는 정보들을 가져온다. 대표적인 예시로는 핑, KDA, 시야점수, 오브젝트 처치 등이 있다.
널리 알려져있는 "롤 티어 올리는 방법"과 비교하며 대중적으로 알려진 방법들이 실제로 유의미한지 검증한다.

### 프로젝트에서 선정한 주제
1. 핑으로 소통하는 것이 승률에 영향을 끼치는가
2. 시야점수는 승률에 영향을 끼치는가
3. 오브젝트 처치는 승률에 영향을 끼치는가
4. KDA는 승률에 영향을 끼치는가
5. 팀원들의 역할군 구성은 승률에 영향을 끼치는가
   
주제들을 통해 실제 게임의 승률과 관련이 있는지 플레이어들이 알고있는 일반적인 개념에 접목하여, 인과관계와 상관관계를 살펴본다.

### 역할
한영철 : 팀장, 기획, 데이터 가공 및 분석, 프레젠테이션\
이유민 : Riot Dev에 숙련도 데이터 요청 및 수집, 데이터 시각화\
이현복 : 데이터 시각화 전략 구상, 데이터 시각화\
조성현 : 아이디어, Riot Dev에 매치 데이터 요청 및 수집, 프레젠테이션 자료 제작
