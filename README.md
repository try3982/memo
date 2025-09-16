# 📝 Memo App API

간단한 메모장 기능을 제공하는 REST API 프로젝트입니다.  
사용자는 메모를 생성, 조회, 수정, 삭제할 수 있습니다.

---

## 🚀 프로젝트 개요
- 목표: CRUD 기반 메모장 기능 구현
- 기술 스택: Spring Boot, JPA, MySQL, Lombok
- 주요 기능
  1. 접속 시 전체 메모 목록 조회
  2. 메모 생성
  3. 메모 수정
  4. 메모 삭제

---

## 📌 API 설계

| 기능           | Method | URL              | Request Body    | Response                |
|----------------|--------|------------------|-----------------|-------------------------|
| 메모 생성하기   | POST   | /api/memos       | MemoRequestDto  | MemoResponseDto         |
| 메모 조회하기   | GET    | /api/memos       | -               | List<MemoResponseDto>   |
| 메모 변경하기   | PUT    | /api/memos/{id}  | MemoRequestDto  | Long (메모 ID)          |
| 메모 삭제하기   | DELETE | /api/memos/{id}  | -               | Long (메모 ID)          |

---

## 📂 API 상세

1. 메모 생성하기  
   - POST /api/memos  
   - Request  
     {  
       "title": "오늘 할 일",  
       "content": "스프링 프로젝트 진행하기"  
     }  
   - Response  
     {  
       "id": 1,  
       "title": "오늘 할 일",  
       "content": "스프링 프로젝트 진행하기",  
       "createdAt": "2025-09-16T10:00:00"  
     }  

2. 메모 조회하기  
   - GET /api/memos  
   - Response  
     [  
       {  
         "id": 1,  
         "title": "오늘 할 일",  
         "content": "스프링 프로젝트 진행하기",  
         "createdAt": "2025-09-16T10:00:00"  
       }  
     ]  

3. 메모 변경하기  
   - PUT /api/memos/{id}  
   - Request  
     {  
       "title": "내일 할 일",  
       "content": "API 문서 정리하기"  
     }  
   - Response  
     1  

4. 메모 삭제하기  
   - DELETE /api/memos/{id}  
   - Response  
     1  

---

## ⚙️ 실행 방법

1. 레포지토리 클론  
   git clone https://github.com/username/memo-app.git  
   cd memo-app  

2. 프로젝트 실행  
   ./gradlew bootRun  

3. API 확인  
   http://localhost:8080/api/memos  

---
