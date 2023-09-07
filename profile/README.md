# 명품 브랜드 인스타그램 화제성 분석 프로젝트

인스타그램 API를 통해 데이터 파이프라인을 구축하고, 브랜드의 화제성을 대시보드로 조회한다
<br>

## 1. Project Outline

명품 브랜드의 인스타그램 계정과 관련 해시태그를 수집하여  
브랜드의 활동성과 인지도를 측정하고, 각 브랜드의 고유한 온라인 마케팅 전략을 파악합니다.  
이를 통해 브랜드 간의 차별화를 확인하고 경쟁 우위를 평가하며, 소비자 동향을 파악할 수 있습니다.

### Project Duration

2023.08.07 ~ 2023.09.02 (약 3주)

### Team Members & Roles

| Field \ Name | **이성희 [@gracia10](https://github.com/gracia10)** | **이하윤[@ha6oon](https://github.com/ha6oon)** | **임형우[@Hyuoo](https://github.com/Hyuoo)** |
|:--:|:---:|:---:|:---:|
|**Planning**|데이터 모델링 |데이터 모델링, KPI 정의 |데이터 모델링|
|**Infra**| AWS 네트워크 관리,<br>AWS 데이터/컨테이너 환경 구축, <br>Airflow CI/CD | - |AWS Lambda 관리,<br>  스크래퍼 CI/CD|
|**Scrapping**| - | - |Instagram API 스크래퍼,<br>Lambda Event 스케줄링|
|**ETL**|Airflow ETL Dag 개발,<br>EMR 프로세스 개발,<br>Slack 모듈 개발| - | - |
|**ELT**|-|데이터 마트 모델링,<br>마트 쿼리 작성,<br>Airflow ELT Dag 개발,<br>EMR 프로세스 개발 | 데이터 마트 모델링,<br>마트 쿼리 작성|
|**Visualization**|-| Looker 대시보드 생성| Looker 대시보드 생성|
<br>

## 2. Result (Looker Dashboard)
<img src="./files/BI1.png">
<img src="./files/BI2.png">
<!-- <video src="./files/BI_Video.mp4"> -->

## 3. Tech Stack

| Field | Stack |
|:---:|:---|
| Infra | <img src="https://img.shields.io/badge/AWS Secrets Manager-DF0101?style=flat&logo=Amazon+AWS&logoColor=white"/> <I1gpngc="https://img.shields.io/badge/AWS Secrets Manager-DF0101?style=flat&logo=Amazon+AWS&logoColor=white"/> <img src2spng="https
://img.shields.io/badge/AWS Cloudwatch-FF4F8B?style=flat&logo=amazoncloudwatch&logoColor=white"/> <img src="https://img.shields.io/badge/AWS%20EC2-FF9900.svg?style=flat&logo=Amazon-EC2&logoColor=white"/>|
|Scrapping| <img src="https://img.shields.io/badge/AWS Lambda-FF9900?style=flat&logo=awslambda&logoColor=white"/>|
| ETL & ELT | <img src="https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=Apache%20Airflow&logoColor=white"/> <img src="https://img.shields.io/badge/Spark-FAFAFA?style=flat&logo=apache%20spark&logoColor=orange"/> <img src="https://img.shields.io/badge/pydeequ-FAFAFA?style=flat&logo=apache&logoColor=orange"/> |
| Data Storage | <img src="https://img.shields.io/badge/AWS S3-088A08?style=flat&logo=amazons3&logoColor=white"/> <img src="https://img.shields.io/badge/AWS Redshift-8C4FFF?style=flat&logo=amazonredshift&logoColor=white"/> <img src="https://img.shields.io/badge/Snowflake-29B5E8.svg?style=flat&logo=Snowflake&logoColor=white"/> <img src="https://img.shields.io/badge/Amazon%20RDS-527FFF.svg?style=flat&logo=Amazon-RDS&logoColor=white"/>
| BI tool | <img src="https://img.shields.io/badge/Looker-4285F4?style=flat&logo=looker&logoColor=white"/> |
| CI/CD | <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Github Actions-2088FF?style=flat&logo=githubactions&logoColor=white"/> <img src="https://img.shields.io/badge/AWS ECR-FF9900?style=flat&logo=amazonecr&logoColor=white"/> <img src="https://img.shields.io/badge/AWS ECS-FF9900?style=flat&logo=amazonecs&logoColor=white"/> |
| ETC|<img src="https://img.shields.io/badge/Slack-4A154B?style=flat&logo=Slack&logoColor=white"/> <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white"/>|


## 4. Architecture
<img src="./files/Infra.png">

## 5. ERD
__1. RAW_DATA Schema__
<img src="./files/Raw_schema.png">  

__2. Analytics Schema__ 
<img src="./files/Mart_schema.png">

## 6. Modules
| Name | Explanation |
|:---:|:---|
| [LuxuryBrands_Infra]("https://github.com/LuxuryBrands/LuxuryBrands_Infra") | 프로젝트 환경설정과 관련된 모듈 |
| [LuxuryBrands_DataCollector]("https://github.com/LuxuryBrands/LuxuryBrands_DataCollector") | API Scrapper 모듈 |
| [LuxuryBrands_Airflow]("https://github.com/LuxuryBrands/LuxuryBrands_Airflow") | ETL/ELT 파이프라인 모듈 |
| [LuxuryBrands_Looker]("https://github.com/LuxuryBrands/LuxuryBrands_Looker") | 시각화 설정 모듈 |


## 7. Documnet
프로젝트의 자세한 정보는 아래 문서를 참고하여 주시길 바랍니다
- [프로젝트_보고서.pdf](files/project_report.pdf)