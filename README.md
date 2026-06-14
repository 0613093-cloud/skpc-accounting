# 서부광성교회 회계 시스템 (SKPC Accounting)

서부광성교회 재정팀을 위한 웹 기반 회계 관리 시스템입니다.

---

## ✨ 주요 기능

| 기능 | 설명 |
|------|------|
| 📋 헌금 입력/조회 | 헌금유형별 입력 (입력1·2·3), 기간별 필터 조회 |
| 💸 지출 입력/조회 | 부서별 지출, 수취자 계좌 자동완성 |
| 🤝 찬조 관리 | 찬조 유형별 입력 및 집계 |
| 📊 주별/월별 보고 | 헌금 통계, 월간 수지 보고 |
| 🧾 이체확인서 | 지출 내역 영수증 출력 |
| 🏦 잔액비교 | 은행 실잔액 vs 장부 비교 |
| 📤 엑셀 내보내기 | 헌금·지출·찬조 각각 또는 전체 xlsx 저장 |
| 📥 엑셀 불러오기 | xlsx 파일 업로드로 데이터 복원 |
| 🔥 Firebase 실시간 동기화 | 여러 기기에서 동일 데이터 공유 |

---

## 🚀 배포 방법 (GitHub + Vercel, 약 10분)

### 1단계 — GitHub 저장소 만들기

1. [https://github.com](https://github.com) 로그인
2. 우측 상단 **`+`** → **New repository** 클릭
3. 설정:
   - Repository name: `skpc-accounting`
   - **Private** 선택 *(교회 재정 자료 보안을 위해 Private 권장)*
   - README 체크 해제
4. **Create repository** 클릭

---

### 2단계 — 파일 업로드

저장소 페이지 → **`Add file`** → **`Upload files`** 클릭 후
아래 3개 파일을 드래그 업로드:

```
index.html     ← 회계 시스템 본체
vercel.json    ← Vercel 배포 설정
README.md      ← 이 파일
```

**Commit changes** 클릭

---

### 3단계 — Vercel 배포

1. [https://vercel.com](https://vercel.com) → **GitHub 계정으로 로그인**
2. **`Add New → Project`** 클릭
3. `skpc-accounting` 저장소 → **`Import`**
4. Framework Preset: **`Other`** 선택
5. **`Deploy`** 클릭 → 약 1~2분 후 완료

배포 완료 후 접속 주소 예시:
```
https://skpc-accounting.vercel.app
```

---

### 4단계 — 이후 업데이트

파일을 수정할 경우 GitHub에 `index.html`을 덮어쓰면 **Vercel이 자동 재배포**합니다.

---

## 🔒 보안 설정 (권장)

교회 재정 자료이므로 접근 제한을 권장합니다.

**Vercel Password Protection:**
1. Vercel 프로젝트 → **Settings** → **Security**
2. **Password Protection** 활성화 후 비밀번호 설정

---

## 🔥 Firebase 연동 안내

현재 Firebase Firestore 실시간 동기화가 연동되어 있습니다.
- 여러 기기(PC, 태블릿, 스마트폰)에서 **동일한 데이터** 공유
- 인터넷 연결 시 자동 저장 및 동기화
- 오프라인 시에도 localStorage로 동작 (재연결 시 동기화)

---

## 📁 파일 구조

```
skpc-accounting/
├── index.html      ← 회계 시스템 본체 (단일 파일 앱)
├── vercel.json     ← Vercel 배포 설정
└── README.md       ← 이 파일
```

---

## 📞 문의

서부광성교회 재정부
