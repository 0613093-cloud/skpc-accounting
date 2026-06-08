# 서부광성교회 회계 시스템

서부광성교회(SKPC) 재정 관리를 위한 웹 기반 회계 시스템입니다.

---

## 🚀 배포 방법 (GitHub + Vercel)

### 1단계 — GitHub 저장소 만들기

1. [https://github.com](https://github.com) 로그인
2. 우측 상단 **`+`** → **New repository** 클릭
3. 설정:
   - Repository name: `skpc-accounting` (원하는 이름)
   - **Public** 또는 **Private** 선택
   - ✅ **Add a README file** 체크 해제 (이미 있으므로)
4. **Create repository** 클릭

---

### 2단계 — 파일 업로드 (GitHub)

**방법 A: 웹에서 직접 업로드 (가장 쉬움)**

1. 생성된 저장소 페이지에서 **`Add file`** → **`Upload files`** 클릭
2. 이 폴더의 파일들을 모두 드래그 앤 드롭:
   - `index.html`
   - `vercel.json`
   - `README.md`
3. **`Commit changes`** 클릭

**방법 B: Git 명령어 (선택사항)**

```bash
git init
git add .
git commit -m "SKPC 회계 시스템 초기 배포"
git branch -M main
git remote add origin https://github.com/[유저명]/skpc-accounting.git
git push -u origin main
```

---

### 3단계 — Vercel 배포

1. [https://vercel.com](https://vercel.com) 접속 → **GitHub 계정으로 로그인**
2. 대시보드에서 **`Add New...`** → **`Project`** 클릭
3. GitHub 저장소 목록에서 **`skpc-accounting`** 찾아 **`Import`** 클릭
4. 설정 화면:
   - **Framework Preset**: `Other` 선택
   - 나머지는 기본값 유지
5. **`Deploy`** 클릭
6. 1~2분 후 배포 완료! ✅

배포 완료 후 주소 예시:
```
https://skpc-accounting.vercel.app
```

---

### 4단계 — 이후 업데이트

파일을 수정하면 GitHub에 다시 업로드하면 **Vercel이 자동으로 재배포**합니다.

1. GitHub 저장소 → `index.html` 클릭
2. ✏️ 연필 아이콘 클릭 → 편집 또는
3. **`Add file`** → **`Upload files`** 로 새 파일 덮어쓰기
4. **`Commit changes`** → Vercel 자동 재배포

---

## 📁 파일 구조

```
skpc-accounting/
├── index.html      ← 회계 시스템 본체 (단일 파일 앱)
├── vercel.json     ← Vercel 배포 설정
└── README.md       ← 이 파일
```

---

## ⚠️ 데이터 저장 안내

이 앱은 **브라우저 localStorage**에 데이터를 저장합니다.

- 같은 브라우저/기기에서 데이터가 유지됩니다
- 다른 기기에서 사용하려면 **⚙️ 관리 → 데이터 → 📤 내보내기** 로 백업 후 이동하세요
- 브라우저 캐시 삭제 시 데이터가 사라질 수 있으니 **정기 백업** 권장합니다

---

## 🔒 보안 (Private 저장소 권장)

교회 재정 자료이므로 GitHub 저장소를 **Private**으로 설정하고,  
Vercel에서 **Password Protection** 기능 사용을 권장합니다.

Vercel Password Protection 설정:
1. Vercel 프로젝트 → **Settings** → **Security**
2. **Password Protection** 활성화
3. 비밀번호 설정

---

## 📞 문의

서부광성교회 회계부
