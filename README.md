<center><img width=100% src="https://github.com/hkyuuu00/SeoulParkingArea/assets/155419559/030d8295-78b6-495e-9536-bd293465a2da"></center><br/>

# 서울시 주차장 실시간 검색 서비스

### 📖 프로젝트 개요
서울에는 유입되는 차량이 많고 주차장에 주차공간이 다 차있는 경우가 있음.<br/>
이런 문제를 바탕으로 주차장을 조회하여 실시간으로 주차장의 잔여 주차공간이 얼마나 되는지 확인할 수 있도록 서비스를 계획.
<br/>
### 🚀 프로젝트 목표
서울시 시영 주차장 API를 활용하여 실시간으로 주차장의 공간을 조회할 수 있는 서비스를 구현.
<br/><br/><br/>

## 📝 프로젝트 설명

### 💼 기능
서울시 주차장 실시간 검색 서비스는 서울시의 자치구를 검색하여 주차장의 위치정보를 지도로 보여주고 가격, 운영시간, 실시간으로 주차공간을 확인할 수 있는 서비스
<br/>
### 🗺 기술 설계도
<img width=100% src="https://github.com/hkyuuu00/SeoulParkingArea/assets/155419559/17716c4b-b173-4813-9323-6d5523b1e354"><br/><br/>


### 💻 기술 스택
- **FrameWork** &nbsp;&nbsp;![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
- **Frontend** &nbsp;&nbsp;![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
- **Backend** &nbsp;&nbsp;![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
- **Tools** &nbsp;&nbsp;![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
<br/>


### ✨ 주요 기능 및 이미지
<img width=100% src="https://github.com/hkyuuu00/SeoulParkingArea/assets/155419559/d914d171-844c-4301-a963-2677f92968bd"><br/><br/>
- **검색:** 검색창에 자치구를 검색 (ex. 강남구), 입력값이 없이 검색하면 전체 주차장 검색<br/>
- **조회:** 주차장 이름과 주소, 현재 주차장의 실시간 데이터를 리스트로 구현<br/>
- **상세정보:** 주차장 이름을 클릭하여 주차장 상세정보 팝업창을 띄울 수 있음<br/><br/><br/>


<img width=100% src="https://github.com/hkyuuu00/SeoulParkingArea/assets/155419559/4a175e5c-685f-4947-8f1b-bf0cb35e38ed"><br/><br/>
- **위치정보:** 해당 주차장의 위치정보를 지도를 통해 확인<br/>
- **상세정보:** 요일별 운영 시간과 시간별 금액을 확인할 수 있으며, 실시간 주차 공간을 확인 가능<br/><br/><br/>


### 🛠 문제 해결 과정
⚠️ 지도 API 호출 비동기 처리
<table>
  <tr>
    <td>
    <strong>문제</strong>
    </td>
    <td><strong>상세정보 창에서 처음 실행할 때에 지도를 불러오지 못함</strong></td>
  </tr>
  <tr>
    <td>원인</td>
    <td>페이지가 로딩되기전에 지도API 요청값을 받아오기에 지도를 불러오지 못함</td>
  </tr>
  <tr>
    <td>해결</td>
    <td>지도API를 요청하는 함수에 TimeOut을 걸어 페이지가 로드된 후 지도API 요청값을 받아오도록 구현</td>
  </tr>
</table>

<br/><br/>

## ⚙️ 프로젝트 설치 및 실행 방법

### 📝 필요한 작업
- Java 21 환경변수 설정
- <a href="https://data.seoul.go.kr/dataList/OA-13122/A/1/datasetView.do;jsessionid=11A5AF72A8C9ABA56290C26298AFE347.new_portal-svr-21">서울시 시영주차장 API</a> Key 발급
- <a href="https://apis.map.kakao.com/web/">Kakao MAP API</a> Key 발급
- ParkingSearchController.java와 parkingInfo.html에 API Key 추가
- Maven 의존성 설치해주고 SpringBoot 서버 실행

