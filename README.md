# 위드로우 토핑 MVP

목재 맞춤 커팅 주문 플랫폼 (위드로우 토핑 클론)

## 📋 프로젝트 개요

사용자가 목재 치수를 입력하고 다양한 가공 옵션을 선택하여 실시간 3D 미리보기와 견적을 확인할 수 있는 웹 애플리케이션입니다.

## 🎯 구현된 기능

### Step 1: 목재 선택
- 두께 선택 (15mm/18mm/21mm)
- 폭/길이 입력 (mm 단위)
- 3D 미리보기

### Step 2: 가공 옵션
- 기본 원형 가공 (컷팅/포켓)
- 실시간 3D 반영
- 여러 가공 동시 선택 가능

### 원형 가공 상세 기능
- **컷팅 가공**: 관통 구멍 (빨간 테두리)
- **포켓 가공**: 얕은 홈 (파란 테두리)
- 위치 입력 (가로 a, 세로 b)
- 원 지름 입력 (c)
- **실시간 3D 미리보기**: 입력값 변경 시 즉시 반영
- 여러 원형 추가/삭제 가능
- 요청사항 입력

### 실시간 견적
- 재료비 자동 계산 (면적 기반)
- 가공비 자동 추가 (원형 1개당 3,000원)
- 총 견적 표시

## 🛠 기술스택

- **Three.js** - 3D 렌더링
- **Tailwind CSS** - 스타일링
- **Vanilla JavaScript** - 상태 관리

## 🚀 실행 방법

### 로컬 실행
```bash
# 파일 다운로드
git clone https://github.com/2ndlifeinc/wedraw-topping-mvp.git
cd wedraw-topping-mvp

# 브라우저로 열기
open topping-with-holes.html
# 또는 더블클릭
```

### 웹 서버 실행 (선택)
```bash
# Python 3
python3 -m http.server 8080

# Node.js
npx serve .

# 브라우저에서 http://localhost:8080/topping-with-holes.html 열기
```

## 📁 파일 구조

```
wedraw-topping-mvp/
├── topping-with-holes.html      # 최신 버전 (3D 구멍 반영)
├── topping-full.html             # 기본 원형 가공
├── topping-viewer-v2.html        # 가공 옵션 선택
├── topping-viewer.html           # 기본 버전
└── README.md
```

## 🎨 주요 화면

### 1. 목재 선택
- 두께/폭/길이 입력
- 3D 미리보기

### 2. 가공 옵션
- 가공 종류 그리드
- 선택된 가공 목록

### 3. 원형 가공 모달
- 위치 입력 (가로/세로)
- 원 지름 입력
- 3D 실시간 반영
- 여러 원형 추가

## 💡 개발 노트

### 3D 구멍 표현 방식
- **컷팅 가공**: `CylinderGeometry` + `TorusGeometry` (테두리)
- **포켓 가공**: 얕은 `CylinderGeometry` + 테두리
- 실시간 업데이트: 입력 필드 `input` 이벤트 리스너

### 가격 계산
- 재료비: (폭 × 길이) / 1,000,000 × 50,000원
- 가공비: 원형 개수 × 3,000원

## 📝 TODO

- [ ] 다른 가공 옵션 추가 (사각 컷팅, 코너 라운딩 등)
- [ ] 실제 이미지로 가공 그리드 교체
- [ ] 주문서 생성 기능
- [ ] 이메일 발송
- [ ] 결제 연동
- [ ] 관리자 페이지

## 🔗 배포

### Vercel (추천)
1. Vercel 계정 연결
2. Import Git Repository
3. `https://github.com/2ndlifeinc/wedraw-topping-mvp`
4. Deploy 클릭

### GitHub Pages
```bash
# Settings → Pages → Source: main branch
# https://2ndlifeinc.github.io/wedraw-topping-mvp/topping-with-holes.html
```

## 👥 팀

- 개발: 인생2막 팀
- 디자인 참고: 위드로우 토핑 (topping.wedraw.kr)

## 📄 라이선스

MIT License
