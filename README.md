# 🔬 반도체 플라즈마 공정 엔지니어를 위한 대화형 AI 의사결정 지원 서비스

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white"/>
</p>

<br/>

> 복잡한 전문 SW·반복 실험 없이, 채팅 한 줄로  
> **자연어 만으로 플라즈마 공정 예측·최적화·비교·질의응답을 즉시 수행하는 대화형 AI 서비스**

<br/>

## 📺 시연 영상




https://github.com/user-attachments/assets/5240881b-78b6-4553-95a4-d33adb43b89c





<br/>

## 1. 프로젝트 소개

플라즈마 공정 엔지니어는 원하는 결과를 얻기 위해 수십 개의 파라미터를 직접 입력하고, 결과를 확인하고, 다시 조정하는 반복 작업을 해야 한다. 숙련된 엔지니어도 시간이 많이 걸리고, 입력 오류도 빈번하다.

이 서비스는 그 과정을 자연어 대화 한 줄로 대체한다. 사용자가 조건을 말하면 AI가 파라미터를 추출하고, XGBoost 모델로 결과를 예측하며, LLM이 결과를 자연어로 해설해준다.

세종대학교 소프트웨어학과 캡스톤 디자인 프로젝트 (2026 4-1)

### 사용자 인터페이스
<img width="3390" height="1908" alt="영상 1" src="https://github.com/user-attachments/assets/dce5fcd5-8b59-405f-b276-674453c9e926" />

<img width="3390" height="1908" alt="영상 2" src="https://github.com/user-attachments/assets/0b87d215-222d-4bbe-85bb-785b8c2fb447" />

<img width="2400" height="1554" alt="영상 3" src="https://github.com/user-attachments/assets/e492655a-7da4-4922-a526-b51b4205b2f8" />



(무료 영상 편집 툴 vrew를 사용했습니다)

<br/>

## 2. 주요 기능

<img width="3390" height="1908" alt="영상-_4_" src="https://github.com/user-attachments/assets/3616c360-4c2d-43fd-a719-1179fcc5848f" />


| 기능 | 설명 |
|------|------|
| **예측** | 공정 조건을 입력하면 플라즈마 물리량과 식각 성능(Etch Score)을 예측 |
| **최적화** | Optuna 기반으로 성능이 더 좋은 조건 조합을 자동 탐색해 상위 후보 최대 3개 추천 |
| **비교** | 두 공정 조건의 물리량·그래프 차이를 나란히 보여주고 우열을 설명 |
| **질의응답** | RAG 기반 도메인 지식 검색으로 공정 개념과 결과 해석을 자연어로 응답 |

<br/>

## 3. 시스템 아키텍처

### 전체
<img width="1299" height="535" alt="시스템 아키텍처" src="https://github.com/user-attachments/assets/631f9059-5390-470e-9831-14cc58cb7a94" />

### 백엔드
<img width="1664" height="1090" alt="image" src="https://github.com/user-attachments/assets/ee25687d-46af-4690-834f-482203d99733" />


| 파트 | 구성 |
|------|------|
| **Frontend** | React, TypeScript, Chart.js — Vercel 배포 |
| **Backend** | Spring Boot, JPA, AWS EC2 + Docker + Nginx (Blue-Green 배포) + RDS(MySQL) |
| **AI Server** | FastAPI, XGBoost, Optuna, ChromaDB, Qwen LLM — NVIDIA DGX Spark |

<br/>

## 4. 기술 스택

### Backend
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chart.js&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

### AI Server
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189AB4?style=flat-square)
![Optuna](https://img.shields.io/badge/Optuna-6C63FF?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat-square)
![Qwen](https://img.shields.io/badge/Qwen_LLM-612EAF?style=flat-square)

<br/>

## 5. 팀원 소개 및 역할

| 이름 | 역할 | 담당 |
|------|------|------|
| **김원준** | AI | 자연어 이해 및 파라미터 추출, XGBoost 예측 모델, Optuna 최적화, RAG 기반 질의응답, LLM 결과 설명 생성, FastAPI 파이프라인 |
| **임상수** | Backend | REST API 설계 및 구현, 채팅 세션/메시지 관리, 파라미터 검증·재검증·확정 흐름, 응답 DTO 설계, 예외 처리, Blue-Green 무중단 배포 |
| **염지환** | Backend | AI 서버 파이프라인 연동, 컨텍스트 저장, 예측/최적화/비교 결과 데이터 조합, 그래프 데이터(IED/IAD/parameter impact) DB 적재 및 조회 |
| **하지향** | Frontend | React/TypeScript 기반 전체 화면 구현, 채팅 UI, 세션 사이드바, 예측/최적화/비교 결과 패널, 백엔드 API 연동, 상호작용 흐름 구현 |

<br/>


## 8. 레포지토리 구조

```
capstone-plasma/
├── backend/     → Spring Boot (plasma-be)
├── frontend/    → React + TypeScript (plasma-fe)
└── ai/          → FastAPI + XGBoost + Qwen (plasma-ai)
```

| 파트 | 링크 |
|------|------|
| Backend | [sejong-capstone-plasma/plasma-be](https://github.com/sejong-capstone-plasma/plasma-be) |
| Frontend | [sejong-capstone-plasma/plasma-fe](https://github.com/sejong-capstone-plasma/plasma-fe) |
| AI | [sejong-capstone-plasma/plasma-ai](https://github.com/sejong-capstone-plasma/plasma-ai) |

<br/>


---

<p align="center">세종대학교 소프트웨어학과 · 2026 4-1 캡스톤 디자인</p>
