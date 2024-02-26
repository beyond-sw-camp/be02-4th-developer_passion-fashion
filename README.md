![header](https://capsule-render.vercel.app/api?type=Waving&color=F7BE81&height=250&section=header&text=👕LONUA👕&desc=All%20For%20Individual%20Customized%20Fashion&descSize=20&descAlign=50&descAlignY=70&fontSize=100&animation=fadeIn&fontColor=B404AE)

> **[플레이 데이터] 한화시스템 BEYOND SW캠프/ D.P (💥Developer Passion💥)**

<br>

### 🤼‍♂️팀원 소개

<br><br>

&nbsp;　&nbsp;　&nbsp;　&nbsp;　&nbsp;　&nbsp;　&nbsp;　&nbsp;　 🐻 **[이동규](https://github.com/PTCman)**&nbsp;　 🦁 **[김태윤](https://github.com/thanks9807)** &nbsp;　 🐶 **[유형도](https://github.com/hyungdoyou)** &nbsp;　 🐯 **[정원준](https://github.com/Wonjunmar)** &nbsp;　 🐺 **[김경미](https://github.com/asasd)**
<br><br><br><br><br>

## ✨ 프로젝트 기본 소개

- 온라인 쇼핑몰 이용자 수가 **"지속적으로 증가"** 하고 있는만큼, 쇼핑몰에 등록되는 상품의 수 역시  
  **"기하급수적으로 늘어나"** &nbsp;&nbsp;상품 선택 시 이용자가 **선택의 어려움**을 겪고 있다.

- 따라서 **개인에게 맞는 옷, 스타일을 제공**하여 수많은 상품에 대한 선택의 폭을 줄임으로써  
  **쇼핑시간을 단축** 시켜주는 **<span style="color:blue">"개인 맞춤형 패션 플랫폼 서비스"</span>** 를 제공한다.

<br>

---
## 📌 프로젝트 목표
Docker, K8S, Jenkins를 활용하여 기존에 만들었던 Frontend와 Backend프로젝트에 CI/CD를 적용한다.


## :question: CI/CD 필요성

#### 기존 프로젝트 현황
- 개발자가 Git과 같은 분산형 프로그램에 push 할 시 코드에 대한 신뢰성을 보장 할 수 없다. (CI 필요성 대두)
- 개발자가 개발용 컴퓨터에서 직접 빌드를 하고 배포용 컴퓨터에 배포파일을 옮겨 배포를 해야하는 불편함이 있었다. (CD 필요성 대두)
  
## :star: CI/CD 기대효과
- CI를 통해 애플리케이션 변경 사항이 자동으로 버그 테스트를 거치고 레포지토리에 업로드 되어 신뢰성 높은 환경을 구성 할 수 있고 항시 배포 가능한 환경이 된다.
- CD는 개발자가 레포지토리에 있는 애플리케이션을 수분내에 지속적으로 배포함으로써 수동으로 배포할 때 보다 시간을 절약 할 수 있다.
<br>

## 📌 기술 스택

<br>

&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white&color=black"></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=Git&logoColor=white&color=ffa500"></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white"/></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=black&color=blue"/></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=Kubernetes&logoColor=blue&color=skyblue"/></a></a>

---

<br>

## 💾 프로젝트 설계

<br>

### 💡&nbsp;&nbsp;시스템 아키텍처

<br>

<img width="593" alt="화면 캡처 2024-02-25 195936" src="https://github.com/beyond-sw-camp/be02-4th-developer_passion-fashion/assets/148875644/7383caa9-037b-470a-adc1-cc515ea11958">

<br>

### 시나리오

### 1. ㅇㅇㅇ

---

<br>

### 💽&nbsp;&nbsp;CI/CD 시스템 아키텍처

<br>

<img width="595" alt="화면 캡처 2024-02-25 195936" src="https://github.com/beyond-sw-camp/be02-4th-developer_passion-fashion/assets/148875644/37cb8f83-0455-4884-911c-a7f23f38e9bc">

<br>

### 시나리오

### 1. ㅇㅇㅇ

---

<br>

### 📁 &nbsp;&nbsp;k8s 클러스터 구성도

<br>

![k8s 클러스터 구성 아키텍처](https://github.com/beyond-sw-camp/be02-4th-developer_passion-fashion/assets/148875644/a5da4b34-27f3-4800-bd2b-e886c79986e9)

<br>

### 설명

### Master Node

### Worker Node

---

<!-- ## 💻 기능 명세서

<br>
<br>

<details>
<summary><b>🤵🏻‍♂️ 판매자</b></summary><br>
    <div>
    	 <details>
         <summary><b>판매자 회원가입</b></summary>
                  <br>
         <p><b>➡ 판매자가 [ 이메일 아이디, 패스워드, 브랜드명, 브랜드 고유키, 판매자명 ] 을 입력하여 회원가입한다. <br><br>
         <p><img src="https://github.com/beyond-sw-camp/be02-2nd-developer_passion-fashion/assets/148875644/81fa9faa-a9ed-4a73-a487-7f822004922d"/></p>
         </details><br>
    	 <details>
         <summary><b>판매자 로그인</b></summary>
                  <br>
         <p><b>➡ 판매자가 [ 이메일 아이디, 패스워드 ] 를 입력하여 로그인한다.</b></p><br>
         <p><img src="https://github.com/beyond-sw-camp/be02-2nd-developer_passion-fashion/assets/148875644/6de7b500-7ac2-43b9-b9a9-6cdea32c4e76"/></p>
         </details><br>
	    <details>
         <summary><b>판매 상품 등록</b></summary>
                  <br>
         <p><b>➡ 브랜드(판매자)가 [ 브랜드명, 카테고리, 스타일, 상품명, 상품수량, 가격, 상의 및 하의에 대한 치수,<br>
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;상품 이미지 및 상품 설명 이미지 ] 를 입력하여 판매 상품을 등록한다.</b></p><br>
         <p><img src="https://github.com/hyungdoyou/LONUA_Project/assets/148875644/a2c60f39-efe1-4ffa-916b-f88726e397f7"/></p>
         </details><br>
    </div>
</details>

--- -->
