# 개발 가이드

## 개발 환경 설정

### 필수 요구사항

- Python 3.8+
- Django 4.x
- [기타 요구사항 추후 추가]

### 로컬 개발 환경 구성

1. **저장소 클론**
   ```bash
   git clone [repository-url]
   cd yongma
   ```

2. **가상환경 생성 및 활성화**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   # venv\Scripts\activate  # Windows
   ```

3. **의존성 설치**
   ```bash
   pip install -r requirements.txt
   ```

4. **환경 변수 설정**
   ```bash
   cp .env.example .env
   # .env 파일 편집
   ```

5. **데이터베이스 설정**
   ```bash
   python manage.py migrate
   python manage.py createsuperuser
   ```

## 코딩 스타일

### Python/Django 규칙
- PEP 8 스타일 가이드 준수
- Django 베스트 프랙티스 따르기
- [추가 규칙 정리 예정]

### 코드 검사
```bash
# 린트 검사
flake8 .

# 포맷팅
black .

# 타입 검사 (if using)
mypy .
```

## 브랜치 전략

- `main`: 프로덕션 코드
- `develop`: 개발 브랜치
- `feature/기능명`: 새로운 기능 개발
- `bugfix/버그명`: 버그 수정

## 커밋 메시지 규칙

```
type: subject

body (optional)

footer (optional)
```

### Type 종류
- `feat`: 새로운 기능
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 스타일 변경
- `refactor`: 리팩토링
- `test`: 테스트 코드

## 테스트

```bash
# 모든 테스트 실행
python manage.py test

# 특정 앱 테스트
python manage.py test [app_name]

# 커버리지 확인
coverage run --source='.' manage.py test
coverage report
```

## 배포

[배포 방법 추후 추가]

## 문제 해결

### 자주 발생하는 문제들

1. **데이터베이스 연결 오류**
   - [해결 방법 추후 추가]

2. **정적 파일 문제**
   - [해결 방법 추후 추가]

## 추가 정보

- [Django 공식 문서](https://docs.djangoproject.com/)
- [프로젝트 관련 추가 자료 예정]