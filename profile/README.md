# Mongle (몽글)
<img width="250" alt="mongle_logo" src="https://github.com/user-attachments/assets/28e51d69-50b8-4609-a2c4-7e25df43b600" />

🏫 **대학생활 궁금증 해결 AI 플랫폼**

### 🔗 Service Links
<a href="https://apps.apple.com/kr/app/%EB%AA%BD%EA%B8%80-mongle/id6753180069">
  <img src="https://github.com/user-attachments/assets/a708fdb4-ef98-4ba5-af5d-cbd2c81b8e9a" width="20" height="20" alt="ios_icon" /> iOS (App Store)
</a>
<br/>
<a href="https://play.google.com/store/apps/details?id=com.mongle">
  <img src="https://github.com/user-attachments/assets/57ecbd17-9ac7-4478-a34e-64d116aee23f" width="20" height="20" alt="android_icon" /> Android (Play Store)
</a>

<br/>

### 📂 Repositories
* **Frontend**: [MONGLE_FLUTTER](https://github.com/map-community/MONGLE_FLUTTER)
* **Backend**: [MONGLE_SERVER](https://github.com/map-community/MONGLE_SERVER)
* **AI**: [CHATBOT-AI](https://github.com/map-community/CHATBOT-AI)

---

### 서비스 요약
**Mongle** - AI 챗봇의 즉답과 재학생들의 집단지성으로 학교 생활의 모든 궁금증을 해결하는 지식 플랫폼

### 주제 구분
생성형 AI와 커뮤니티를 결합한 대학 특화 질의응답(Q&A) 서비스

### 팀원 소개

| 이름 | 역할 (Role) | 담당 분야 (Responsibility) |
|:---:|:---:|:---|
| **박신영** | **Team Leader** | Frontend (Flutter), AI Engineering (RAG/MSA), Orchestration |
| **김대건** | **PM & Design** | Project Manager, Service Planning, UI/UX Design |
| **이원준** | **Backend Leader** | Server Architecture, Core Logic Design, Database Modeling |
| **최기영** | **Backend Dev** | API Development, Service Logic Implementation |
| **현지혜** | **Backend Dev** | API Development, Data Management |

---

### 서비스 소개

#### 서비스 개요
* **AI 챗봇:** 학사 일정, 규정, 연락처 등 'Fact' 기반의 정보를 AI가 RAG(검색 증강 생성) 기술로 즉시 답변
* **지도 기반 커뮤니티:** AI가 답하기 힘든 "학생회실 위치", "실시간 상황" 등의 질문을 지도 위에 핀을 꽂아 질문하고 답변받는 하이퍼 로컬 커뮤니티
* 현재는 AI 답변 기능과 커뮤니티 기능이 독립적으로 구성되어, 사용자가 목적에 맞게 선택하여 활용 가능

#### 타 서비스와의 차별점
* **기존 커뮤니티(에브리타임 등):** 반복되는 질문으로 인한 기존 유저의 피로감 누적, 정보 검색의 어려움
* **Mongle:**
    * 단순 정보는 AI가 3초 만에 답변하여 불필요한 질의응답 감소
    * 그 외 질문은 QnA 커뮤니티에서 유저를 통해 해결

---

### 구현 내용 및 결과물

* **AI 챗봇 (RAG & VLM)**
    * 학교 공지사항, 규정 PDF 등을 학습하여 정확한 출처와 함께 답변 제공
    * 텍스트뿐만 아니라 이미지 정보 처리 가능
    * MSA(Microservices Architecture) 적용으로 AI 모델 서버를 별도 분리하여 운영
* **지도 기반 커뮤니티 (Hyper-local)**
    * 사용자가 원하는 위치에 핀을 찍어 질문 등록 (익명 보장)
    * 해당 위치 주변 사용자들에게 노출되어 정확한 로컬 정보 획득 가능

#### 구현 사진

<table>
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/c8b789ea-904d-4175-ae11-9241531e6a2c" width="100%"></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/d8b2e3ab-80e7-4e18-b746-00e1a8258876" width="100%"></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/9f57b070-c88d-4ed0-acf8-9f1d9a5ab6d0" width="100%"></td>
  </tr>
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/4c12e3f2-ef6f-4bc6-b72c-637a20eed815" width="100%"></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/687a7a85-5ea6-4610-89a5-82db586f75e3" width="100%"></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/7470ef05-2dad-4fe2-bb1e-559cc8e47991" width="100%"></td>
  </tr>
</table>

### 구현 방식 (Tech Stack)
<img width="800" alt="tech_stack" src="https://github.com/user-attachments/assets/7f7b3dd3-8617-411f-916f-7d04858fe86d" />

* **App Architecture:** Feature-first Architecture (기능 중심 설계)
* **Frontend:** Flutter (IOS, Android Cross-platform)
* **Backend (Main):** Java, Spring Boot
* **AI Backend (MSA):** Python, FastAPI, AWS EC2
* **AI Tech:** RAG (Retrieval-Augmented Generation), VLM, Vector DB
* **Orchestration:** Claude 등 AI Coding Assistant를 활용하되, 아키텍처 설계 및 로직 검증, PR 승인은 인간 개발자(Team Leader)가 주도하는 오케스트레이션 개발 방법론 적용

---

### 향후 개선 혹은 발전 방안 (Planned)

* **데이터 선순환 구조(Data Flywheel) 구축**
    * 현재 분리되어 있는 '커뮤니티'와 'AI'를 연동
    * 커뮤니티에서 학생들이 남긴 양질의 답변 데이터를 AI가 다시 학습하여, 시간이 지날수록 AI가 똑똑해지는 자동화 파이프라인 구축 예정
* **광고 시스템 (BM) 도입**
    * 지도 내 특정 구역(건물, 상권)의 광고 권한을 경매(Bidding) 방식으로 판매하는 지도 기반 수익 모델 개발 예정
* **서비스 확장**
    * 단과대별 행정 데이터 통합 및 타 대학(경북권)으로 서비스 확장
