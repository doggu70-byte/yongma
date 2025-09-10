# API 문서

## 개요

Yongma 프로젝트의 REST API 문서입니다.

## 기본 정보

- **Base URL**: `http://localhost:8000/api/`
- **API Version**: v1
- **Content-Type**: `application/json`

## 인증

### 인증 방식
- [인증 방식 추후 추가]
- Token Authentication / JWT 등

### 헤더 예시
```http
Authorization: Bearer <token>
Content-Type: application/json
```

## API 엔드포인트

### 사용자 관리

#### 사용자 목록 조회
```http
GET /api/users/
```

**응답 예시:**
```json
{
  "results": [
    {
      "id": 1,
      "username": "user1",
      "email": "user1@example.com"
    }
  ]
}
```

#### 사용자 생성
```http
POST /api/users/
```

**요청 예시:**
```json
{
  "username": "newuser",
  "email": "newuser@example.com",
  "password": "password123"
}
```

### [기타 엔드포인트 추후 추가]

## 응답 코드

| 코드 | 설명 |
|------|------|
| 200 | 성공 |
| 201 | 생성 성공 |
| 400 | 잘못된 요청 |
| 401 | 인증 필요 |
| 403 | 권한 없음 |
| 404 | 찾을 수 없음 |
| 500 | 서버 오류 |

## 에러 응답 형식

```json
{
  "error": {
    "code": "ERROR_CODE",
    "message": "오류 메시지",
    "details": {}
  }
}
```

## 페이지네이션

```json
{
  "count": 100,
  "next": "http://localhost:8000/api/users/?page=2",
  "previous": null,
  "results": [...]
}
```

## 필터링 및 정렬

### 쿼리 파라미터
- `page`: 페이지 번호
- `page_size`: 페이지당 항목 수
- `ordering`: 정렬 필드
- `search`: 검색 키워드

### 예시
```http
GET /api/users/?search=john&ordering=-created_at&page=1&page_size=10
```

## 테스트

### Postman Collection
[Postman 컬렉션 링크 추후 추가]

### 테스트 서버
- **개발**: `http://localhost:8000/api/`
- **스테이징**: [URL 추후 추가]
- **프로덕션**: [URL 추후 추가]

## 변경 이력

| 버전 | 날짜 | 변경 내용 |
|------|------|----------|
| v1.0 | 2024-XX-XX | 초기 버전 |

## 추가 정보

- [Django REST Framework 문서](https://www.django-rest-framework.org/)
- [API 설계 가이드라인 추후 추가]