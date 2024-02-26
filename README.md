![header](https://capsule-render.vercel.app/api?type=Waving&color=F7BE81&height=250&section=header&text=👕LONUA👕&desc=All%20For%20Individual%20Customized%20Fashion&descSize=20&descAlign=50&descAlignY=70&fontSize=100&animation=fadeIn&fontColor=B404AE)

> **[플레이 데이터] 한화시스템 BEYOND SW캠프/ D.P (💥Developer Passion💥)**



<br>

<h1 align="center">데브옵스 아키텍쳐 구현 👍</h1>s

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

## 🖥️ 운영 환경



* 쿠버네티스를 이용한 컨테이너 운영 환경 구성 

쿠버네티스를 이용한 이유  
 1. 유연성
쇼핑몰의 특성상 이벤트와 할인에 따라 트래픽이 몰릴 수 있기 때문에 트래픽 상황에 따라 유연하게 대처할 수 있다는 장점이 있다.

 2. 장애 대처
 

### 💡&nbsp;&nbsp;시스템 아키텍처

<br>

<img width="593" alt="화면 캡처 2024-02-25 195936" src="https://github.com/beyond-sw-camp/be02-4th-developer_passion-fashion/assets/148875644/7383caa9-037b-470a-adc1-cc515ea11958">

<br>

* 프론트엔드, 백엔드, DB 모두 각각의 디플로이먼트를 통해 파드로 생성된다.   
* 사용자들은 LB (LoadBalancer) 타입의 Frontend-svc를 통해 웹 포트로 Nginx 서버에 접근하여 서비스를 이용한다.  
* 파드들 간의 통신은 ClusterIp 타입의 서비스를 통해 내부 통신으로 이루어진다. 따라서 외부에 노출 되지 않는다.


### 📁 &nbsp;&nbsp;k8s 클러스터 구성도

<br>

![클러스터 구성도](./img/clusterArchitecture.jpg)

총 5대의 노드로 클러스터를 구성했다.

<br>
* CNI는 Calico를 통해서 구성하였으며, 그 이유는 아래의 사진에서 볼 수 있 듯이, 성능적으로 뛰어나다는 점과 오픈 소스여서 무료로 이용할 수 있다는 점 2가지이다.

![image](https://github.com/thanks9807/programmers/assets/40519125/ccbbd547-1133-423f-b457-277ae83a2782)


Calico는 LoadBalance type의 서비스를 제공하지 않으므로 metalib를 추가로 사용하게 되었다.

자세한 설명은 클릭해야 볼 수 있게 만들자

각 Worker 노드에는 다음과 같은 파드가 공통적으로 생성된다.
* calico-node :  네트워크 정책을 관리하고 구성하는 역할
* metalib-system : 클러스터 내에서 로드 밸런싱 및 외부 서비스 노출을 담당하는 역할

Master Node에는 다음과 같은 파드들이 추가된다.
> kube-system Namespace
> * coredns : 클러스터 내에서 DNS 서버 역할
> * calico-kube-controllers : 클러스터 내에서 네트워크 정책을 관리하고 구성하는 역할
> * metrics-server : 클러스터 내에서 파드 및 노드의 리소스 사용량 및 성능 지표를 수집하고 노출하는 역할

> metailb-system Namespace
> * speaker :  외부 라우팅 장치와 통신하여 로드 밸런서에 할당된 IP 주소를 라우팅하는 역할
> * controller : 클러스터 내에서 IP 주소 범위를 관리하고, 외부 서비스에 IP 주소를 동적으로 할당하고 회수하는 역할


### 운영 시나리오

<br>

### 💽&nbsp;&nbsp;CI/CD 시스템 아키텍처
<br>

## 📌 기술 스택
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white&color=black"></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=Git&logoColor=white&color=ffa500"></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white"/></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=black&color=blue"/></a></a>
&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=Kubernetes&logoColor=blue&color=skyblue"/></a></a>
<br>

<br>



<br>

## 배포 시나리오

블루-그린 방식을 이용한 무중단 배포 

<img width="595" alt="화면 캡처 2024-02-25 195936" src="https://github.com/beyond-sw-camp/be02-4th-developer_passion-fashion/assets/148875644/37cb8f83-0455-4884-911c-a7f23f38e9bc">



1. 깃허브(원격 저장소) main branch 에 최신 버전의 프로젝트가 push된다.
2. 깃허브는 젠킨스에게 Webhook를 보낸다.
3. 젠킨스는 파이프라인에 저장된 절차를 실행한다.  
  a. 젠킨스 서버에 깃허브의 있는 프로젝트를 가져온다. (git clone)  
  b. 프로젝트가 벡엔드라면 mvn package, 프로젝트가 프론트엔드라면 npm run build를 통해 build한다.  
  c. 빌드를 통해 생긴 jar 또는 dist directory를 이용해 dockerfile로 docker image를 만든다.  
  d. docker image를 docker hub에 올린다.  
  e. 젠킨스 서버에서 k8s master에 deployment와 service를 만드는 yml file을 전송한다.
  f. k8s master에서 yml file들을 적용시킨다. (kubectl apply)
  g. 파이프라인을 진행하면서 단계마다 시작, 종료, 결과를 젠킨스 서버에서 webhook를 통해 slack으로 전송한다.  
  h. slack를 통해 개발자들은 파이프라인 진행 현황을 확인할 수 있다.

4. 블루 그린 방식을 통해 무중단 배포를 한다.
파이프라인의 빌드 번호에 따라 deployment blue또는deployment green이 갱신이 된다.
5. 갱신이 종료된 디플로이먼트를 서비스에 연결 시켜준다.

무중단 배포, 블루 그린 방식을 선택한 이유
소비자들이 소비 욕구를 느꼈을 때, 그 상품을 바로 구매하지 못하면 구매율이 떨어질 수  밖에 없다.
따라서 쇼핑몰은 사용자들이 원하는 시기에 항상 상품을 구매할 수 있도록 해야한다.
따라서 무중단 배포를 선택하였다. 
방식은 레드 그린 방식을 선택했다.
레드 그린 방식이 이점은 이전 버전의 deployment 가 준비되어있다는 점으로, 최신 버전에 문제가 발생되었을 때,
이전 버전으로 빠르게 되돌릴 수 있다.  

---
### 테스트 및 결과
<br>


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
