# 🎯 AI 취업 컨설턴트

AI 기반 취업 컨설팅 챗봇 - 채용 공고 분석, 면접 준비, 이력서 첨삭까지 당신의 커리어를 지원합니다.

## 📋 프로젝트 개요

취업 준비생과 취업 준비생을 위한 올인원 AI 컨설턴트입니다. RAG 기술을 활용한 문서 분석, 실시간 웹 검색, GPT-4 기반 답변 생성을 통해 맞춤형 취업 컨설팅을 제공합니다.

## ✨ 주요 기능

### 📚 RAG 모드 (문서 기반 분석)
- PDF 문서 업로드 및 인덱싱
- 교육과정 안내, 기업 정책 문서 분석
- 벡터 DB 기반 정확한 문서 검색

### 🔍 웹 검색 모드 (최신 정보)
- 네이버 블로그/카페 실시간 검색
- 기업별 채용 공고 및 직무 분석
- 연봉 정보, 면접 후기, 업계 트렌드

### 🧠 AI 직접 답변 (일반 컨설팅)
- 자소서 첨삭 가이드
- 면접 답변 구조화 (STAR 기법)
- IT 개념 설명 및 컨설팅

### 🎯 스마트 모드 전환
- AI가 질문을 자동 분석하여 최적의 답변 모드 선택
- RAG / 웹 검색 / LLM 직접 답변 자동 전환
- 사용자 편의성 극대화

## 🛠 기술 스택

- **Frontend**: Streamlit
- **LLM**: OpenAI GPT-4o-mini
- **RAG**: LangChain + FAISS Vector Store
- **Search API**: Naver Search API (Blog, Cafe)
- **PDF Processing**: PyPDF

## 🚀 설치 및 실행

### 1. 레포지토리 클론
```bash
git clone https://github.com/your-username/ai-job-consultant.git
cd ai-job-consultant
```

### 2. 가상환경 설정
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. 패키지 설치
```bash
pip install -r requirements.txt
```

### 4. API 키 설정

`.streamlit/secrets.toml` 파일 생성:
```toml
OPENAI_API_KEY = "your-openai-api-key"
NAVER_CLIENT_ID = "your-naver-client-id"
NAVER_CLIENT_SECRET = "your-naver-client-secret"
```

**API 키 발급 방법:**
- **OpenAI**: https://platform.openai.com/api-keys
- **Naver**: https://developers.naver.com/apps/#/register

### 5. 실행
```bash
streamlit run app.py
```

브라우저에서 `http://localhost:8501` 접속

## 📁 프로젝트 구조

```
ai-job-consultant/
├── app.py                          # 메인 애플리케이션
├── requirements.txt                # 패키지 목록
├── .streamlit/
│   └── secrets.toml.example       # API 키 템플릿
├── Document/                       # PDF 문서 저장 폴더
├── .gitignore
└── README.md
```

## 🌐 Streamlit Cloud 배포

### 1. GitHub 레포지토리 푸시
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

### 2. Streamlit Cloud 설정
1. https://share.streamlit.io 접속
2. "New app" 클릭
3. GitHub 레포지토리 연결
4. `app.py` 파일 선택
5. **Advanced settings** → **Secrets** 에서 API 키 입력:
   ```toml
   OPENAI_API_KEY = "your-key"
   NAVER_CLIENT_ID = "your-id"
   NAVER_CLIENT_SECRET = "your-secret"
   ```
6. Deploy 클릭

## 💡 사용 가이드

### RAG 모드 활성화
1. 사이드바에서 "문서 인덱싱" 클릭
2. `Document/` 폴더에 PDF 파일 추가
3. 교육/정책 관련 질문 입력

### 웹 검색 활성화
- 검색 소스 선택 (네이버 블로그, 카페)
- 검색 결과 개수 설정
- 최신 채용 정보 질문

### 추천 질문 예시
- "🎯 직무 역량 분석법"
- "💡 면접 대비 방법"
- "📊 연봉/트렌드 확인법"

## 🔒 보안 주의사항

- API 키는 절대 GitHub에 업로드하지 마세요
- `.streamlit/secrets.toml` 파일은 `.gitignore`에 포함
- 민감한 PDF 문서는 `Document/` 폴더에서 관리

## 📊 주요 통계

- 대화 수 추적
- 웹 검색 횟수 모니터링
- 모드별 사용 통계

## 🤝 기여하기

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 라이선스

이 프로젝트는 MIT 라이선스를 따릅니다.

## 📧 문의

프로젝트 관련 문의사항은 이슈를 등록해주세요.

---

**Built with ❤️ using Streamlit & OpenAI**
