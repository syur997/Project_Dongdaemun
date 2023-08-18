![header](https://capsule-render.vercel.app/api?type=Waving&color=A9D0F5&height=200&text=Project&fontColor=FFFFFF)

<h1 align="center"> 👕 동대문 시장 기업 데이터 기반 문제 해결 프로젝트 👖 </h1>
<div align='right'>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> <img src="https://img.shields.io/badge/BigQuery-4285F4?style=flat-square&logo=GoogleCloud&logoColor=white"/> <img src="https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=Tableau&logoColor=white"/> <img src="https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=GoogleColab&logoColor=white"/> <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=Jupyter&logoColor=white"/> 
</div>
<br>
<br>
<br>
<p align="left">
<!--   📄 분석 보고서 노션 링크: https://www.notion.so/64a5c9523cd745729912bef1df693faf?pvs=4 -->
</p>
<br>
<br>
<br>
<h2 align="left"> 주제 및 선정 배경</h2>
<p align="left">
  
  **- 주제: 사입업체와 사입삼촌의 자금 관리 문제점 해결**
  <br>
  <br>
  **- 선정 배경**<br>
  1. 사입삼촌의 일정하지 않은 자금 출처<br>
    - 소매업자에게 입금 받은 돈 → 미리 입금 받지 못하면 사입삼촌의 현금으로 결제<br>
    - 도매업장으로 가기 전, 사입업체에게 받은 돈 → 일하는 중 자금이 부족해지면 사입삼촌의 현금으로 결제<br>
    <br>
  2. 사입삼촌에게 발생하는 외상 상황<br>
    - 도매상이 바빠서 결제할 상황이 되지 않을 때<br>
    - 사입삼촌의 자금 흐름이 원활하지 않아 결제할 현금이 없지만 도매상과 친분이 있어 도매상이 사입삼촌의 사정을 이해해줄 때<br>
    <br>
  3. 사입삼촌의 수기 장부 관리<br>
    - 동대문 시장의 특성상 현금 결제로 이루어짐 → 장부와 영수증을 수기로 작성 → 정확도↓<br>
</p>
<br>
<br>
<br>
<h2 align="left"> 활용 데이터 </h2>
<p align="left">
  1. 해당 기업의 주문 데이터<br>
  2. 해당 기업의 정산 데이터<br>
</p>
<br>
<br>
<br>
<h2 align="left"> EDA 및 분석 </h2>
<p align="left">
  1. 사입업체별 외상대납비<br>
  <img src="https://github.com/syur997/Project_Dongdaemun/assets/110324563/d4694d41-3207-41d1-89f8-b1a60a25888b.png" width="250" height="300"/><br>
  - 사입업체별로 외상유무가 ‘Y’인 대납비의 합계를 확인했을 때 B1 업체가 확연하게 높은 것을 확인<br>
  - 확인 결과, B1 업체는 ‘제주’ 담당 업체였고 B1이 대표성을 띄게 될 것 같아 이상치로 판단<br>
  <br>
  <br>
  2. 사입업체별 외상대납비와 사입업체별 총 외상대납비<br>
  <img src="https://github.com/syur997/Project_Dongdaemun/assets/110324563/97793623-96f2-4bd8-85cd-22b1a40309b5.png" width="550" height="250"/><br>
  - B1 업체를 제거 후 업체별 bar color를 변경하여 5개의 업체를 외상대납비 합계순으로 확인<br>
  - 모든 사입업체의 총 대납비를 확인했을 때, 앞서 확인한 [사입업체별 외상대납비]의 5개의 업체들이 모두 상위 10위 안에 있는 것 확인
  <br>
  <br>
  <br>
  3. 외상 경험이 있는 사입업체별 대납비와 청구 금액<br>
  <img src="https://github.com/syur997/Project_Dongdaemun/assets/110324563/80c9549c-98a7-4fcd-867a-9327c68dd125.png" width="400" height="250"/><br>
  - 외상 경험이 있는 5개 업체의 청구금액과 대납비를 비교해보았을 때, 5개의 업체 모두 대납비가 청구금액의 80%이상이거나 청구금액을 초과하는 것을 확인<br>
  <br>
  <br>
  4. 소매별 평균 외상 납입일<br>
  <img src="https://github.com/syur997/Project_Dongdaemun/assets/110324563/efb4903a-eb07-4cec-bd46-f296a4eb84cc.png" width="200" height="350"/><br>
  - 소매별 평균 외상납입일을 확인 → 평균 2일 소요<br>
  <br>
  <br>
</p>
<br>
<br>
<h2 align="left"> 분석 결과 </h2>
<p align="left">
  - 외상을 하는 사입업체가 모든 사입업체의 총 대납비의 상위 10위 안에 속하므로 총 대납비가 높은 사입업체일수록 외상 할 확률이 높다.<br>
  <br>
  - 외상을 하는 사입삼촌 8명 중 6명이 모든 사입삼촌의 총 대납비 상위 10위 안에 속하므로 총 대납비가 높은 사입삼촌일수록 외상 할 확률이 높다.<br>
  <br>
  - 외상을 하는 사입업체는 대납비가 청구금액의 80% 이상이거나 청구금액을 초과함으로써 외상을 하는 사입업체의 사입삼촌들은 현금 유동성이 떨어질 확률이 높다.<br>
  <br>
  - 소매별 평균 외상납입일은 2일이니 사입업체와 사입삼촌은 자금 계획을 세울 때 외상납입일을 2일로 계산할 수 있다.<br>
  <br>
</p>
<br>
<br>
<br>
<h2 align="left"> 활용 방안 </h2>
<p align="left">
  1. 평균 외상납입일 안내 서비스<br>
    - 주문을 받은 사입삼촌에게 소매상의 평균 외상납입일을 안내함으로써 자금 관리에 도움이 되도록 한다.<br>
  <br>
  2. 누적금액 알림 서비스<br>
    - 외상비 or 대납비가 일정 금액이 될 경우, 사입삼촌에게 알림을 제공함으로써 수기 작성으로 매번 파악하기 힘들었던 누적액을 쉽게 파악하도록 한다.<br>
  <br>
  3. 관심삼촌 알림 서비스<br>
    - 사입삼촌별 대납비가 청구금액의 일정 %를 초과할 경우, 사입삼촌의 사입업체에게 알림을 제공함으로써 사입삼촌을 관리할 수 있도록 한다.<br>
</p>
<br>
<br>

