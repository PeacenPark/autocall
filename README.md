# 에벤에셀 전기수리 - 전화 연결 랜딩 페이지

용인·수원 전역 24시간 긴급 출동 전기 점검 서비스

## 📂 폴더 구조

```
ebenezer-call/
├── index.html          # 메인 페이지 (전화 연결)
├── images/
│   ├── banner.png      # 오픈 그래프 배너 (1200x630)
│   └── profile.png     # 프로필 이미지
└── README.md           # 이 파일
```

---

## 🚀 GitHub Pages 배포 방법

### 1단계: GitHub 저장소 생성

1. https://github.com 로그인
2. 우측 상단 "+" 버튼 → "New repository"
3. 저장소 설정:
   - Repository name: `ebenezer-call` (원하는 이름)
   - Public 선택
   - "Create repository" 클릭

### 2단계: 파일 업로드

#### 방법 A: 웹에서 직접 업로드

1. 저장소 페이지에서 "uploading an existing file" 클릭
2. 이 폴더의 모든 파일을 드래그 & 드롭:
   - `index.html`
   - `images/banner.png`
   - `images/profile.png`
   - `README.md`
3. "Commit changes" 클릭

**중요: images 폴더 구조 유지!**
- images 폴더를 먼저 만든 후
- 그 안에 이미지 파일들 업로드

#### 방법 B: Git 명령어 사용

```bash
# 저장소 클론
git clone https://github.com/사용자명/ebenezer-call.git
cd ebenezer-call

# 파일 복사
# (다운로드한 폴더의 모든 파일을 여기로 복사)

# Git에 추가 및 커밋
git add .
git commit -m "Initial commit"
git push origin main
```

### 3단계: GitHub Pages 활성화

1. 저장소 페이지에서 "Settings" 클릭
2. 왼쪽 메뉴에서 "Pages" 클릭
3. Source 섹션:
   - Branch: `main` 선택
   - Folder: `/ (root)` 선택
4. "Save" 클릭
5. 2-3분 기다리면 배포 완료!

**배포 완료 URL:**
```
https://사용자명.github.io/ebenezer-call/
```

---

## ⚙️ 설정 변경하기

### index.html 파일 수정 필요!

GitHub Pages 활성화 후, `index.html` 파일을 열어서 다음 부분을 수정하세요:

**수정 전:**
```html
<meta property="og:image" content="https://사용자명.github.io/저장소명/images/banner.png">
<meta property="og:url" content="https://사용자명.github.io/저장소명/">
```

**수정 후:**
```html
<meta property="og:image" content="https://peacenpark.github.io/ebenezer-call/images/banner.png">
<meta property="og:url" content="https://peacenpark.github.io/ebenezer-call/">
```

> 💡 **팁**: GitHub 웹에서 직접 수정 가능!
> 1. index.html 클릭
> 2. 연필 아이콘(Edit) 클릭
> 3. 수정 후 "Commit changes"

### 전화번호 변경하기

전화번호를 바꾸고 싶다면 `index.html`에서 `0506-465-0119`를 모두 찾아서 변경하세요.

---

## 📝 네이버 블로그에 링크 넣기

### 1. 블로그 글 작성

```
전기 문제로 고민이시라면?

📞 긴급 상담 신청하기
```

### 2. 링크 삽입

- "긴급 상담 신청하기" 텍스트 드래그
- 링크 버튼 클릭
- URL 입력: `https://peacenpark.github.io/ebenezer-call/`
- 엔터 → 자동으로 배너 미리보기 생성!

### 3. 결과

```
┌─────────────────────────────────────┐
│  [프로필 이미지] 에벤에셀 전기수리   │
│  용인·수원 전역 24시간 긴급 출동    │
│  📞 0506-465-0119                   │
│                                     │
│  peacenpark.github.io/ebenezer-call │
└─────────────────────────────────────┘
```

---

## 🎯 작동 방식

1. **블로그에서 링크 클릭**
2. **GitHub Pages로 이동** (index.html 열림)
3. **자동으로 전화 연결** (tel:0506-465-0119)
4. 실패 시 **수동 버튼 제공**

---

## 🔍 테스트하기

### 배포 후 확인사항:

✅ **페이지 열리는지 확인**
- https://사용자명.github.io/ebenezer-call/ 접속
- 페이지가 정상적으로 보이는지 확인

✅ **이미지 로딩 확인**
- 프로필 이미지가 보이는지 확인
- F12 → Console에서 에러 없는지 확인

✅ **전화 연결 테스트**
- 모바일에서 링크 열기
- 전화 앱이 실행되는지 확인

✅ **링크 미리보기 테스트**
- Facebook Debugger: https://developers.facebook.com/tools/debug/
- URL 입력 후 "Fetch new information"
- 배너 이미지가 제대로 보이는지 확인

---

## 🛠️ 문제 해결

### 문제: 이미지가 안 보여요!

**해결:**
1. GitHub 저장소에서 images 폴더 구조 확인
   ```
   ebenezer-call/
   └── images/
       ├── banner.png
       └── profile.png
   ```
2. 파일명 대소문자 정확히 확인 (banner.png vs Banner.png)
3. 2-3분 기다리기 (GitHub Pages 캐시 갱신 시간)

### 문제: 링크 미리보기에 배너가 안 나와요!

**해결:**
1. index.html의 og:image URL이 정확한지 확인
2. 이미지 URL을 브라우저에서 직접 열어보기
3. Facebook Debugger에서 캐시 새로고침
4. URL 끝에 `?v=2` 추가해서 재시도

### 문제: GitHub Pages가 활성화 안돼요!

**해결:**
1. 저장소가 Public인지 확인
2. main 브랜치에 파일이 올라갔는지 확인
3. Settings → Pages에서 Source가 제대로 설정됐는지 확인

---

## 📊 업데이트 방법

### 내용 수정하기:

1. GitHub 저장소 페이지에서 `index.html` 클릭
2. 연필 아이콘 (Edit) 클릭
3. 내용 수정
4. "Commit changes" 클릭
5. 1-2분 후 자동 반영!

### 이미지 교체하기:

1. images 폴더에서 기존 이미지 삭제
2. 새 이미지 업로드 (같은 파일명 사용)
3. 자동 반영!

---

## 💡 추가 활용

### 짧은 URL 만들기

- **bit.ly** 사용: `bit.ly/ebenezer-call`
- 기억하기 쉽고 공유하기 편함!

### QR 코드 생성

- https://www.qr-code-generator.com
- GitHub Pages URL 입력
- 명함이나 전단지에 활용

### 여러 버전 만들기

- `index.html` → 긴급 출동용
- `consultation.html` → 무료 상담용
- `inspection.html` → 정기 점검용

---

## 📞 연락처

**에벤에셀 전기수리**
- 전화: 0506-465-0119
- 서비스 지역: 용인·수원 전역
- 운영 시간: 24시간 긴급 출동

---

## 📄 라이선스

이 프로젝트는 개인 사업 용도로 자유롭게 사용 가능합니다.

---

**배포 완료 후 꼭 확인하세요!**
1. ✅ GitHub Pages 활성화
2. ✅ index.html의 og:image URL 수정
3. ✅ 실제 URL로 접속 테스트
4. ✅ 모바일에서 전화 연결 테스트
5. ✅ 네이버 블로그에 링크 테스트
