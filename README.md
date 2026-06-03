# 🚀 Neon Space Shooter

> Zero-dependency neon arcade shoot 'em up — pure HTML / CSS / Canvas 2D, no build step.

![preview](media/preview.png)

브라우저에서 바로 실행되는 **레트로 네온 스타일 우주 슈터** 게임입니다.
외부 라이브러리 없이 단일 HTML 파일 (~17KB)로 구성되어 있어요.

🎬 **[홍보 영상 보기](media/promo.mp4)**

---

## ✨ 주요 기능

- 🎯 **3-Way 멀티샷** — 레벨 3·5에서 자동 해금
- 💥 **다이아몬드 보스전** — 500점마다 부채꼴 탄막 보스 등장
- ⚡ **네온 글로우 그래픽** — Canvas `shadowBlur` 기반 발광 효과
- 🪐 **파라랙스 별 배경** — 120개 별의 스크롤 레이어
- 📈 **점진적 난이도** — 시간 기반 자동 레벨업 시스템
- 📱 **터치 지원** — 모바일에서도 드래그/탭 조작 가능
- 🏆 **하이스코어 기록**

## 🎮 조작법

| 키 | 동작 |
|---|---|
| `← →` 또는 `A` `D` | 좌우 이동 |
| `SPACE` 또는 `W` `↑` | 발사 |
| 터치 드래그 / 탭 | 모바일 조작 |

## 🚀 실행 방법

### 1. 바로 열기

```bash
open neon_space_shooter.html
```

### 2. 로컬 서버

```bash
# Python
python3 -m http.server 8080

# Node.js
npx serve .
```

브라우저에서 `http://localhost:8080/neon_space_shooter.html` 접속.

## 🎯 점수 체계

| 적 | 점수 | HP |
|---|---|---|
| 작은 소행성 | 10점 | 1 |
| 큰 소행성 | 30점 | 3 |
| UFO | 50점 | 2~ |
| 💎 보스 | 300점 | 40~ |

## 🏗️ 아키텍처

```
┌─────────────────────────────────────────┐
│  requestAnimationFrame loop             │
│  ┌──────────────┐    ┌──────────────┐  │
│  │   update()   │    │    draw()    │  │
│  │  - 입력      │    │  - 별 배경   │  │
│  │  - 스폰      │    │  - 엔티티    │  │
│  │  - 충돌      │    │  - 파티클    │  │
│  │  - 물리      │    │  - HUD       │  │
│  └──────────────┘    └──────────────┘  │
│         ↓                  ↑            │
│   상태(state): menu / playing / dead    │
└─────────────────────────────────────────┘
```

## 🛠️ 기술 스택

- **HTML5 Canvas 2D API** — 모든 렌더링
- **Vanilla JavaScript** — 외부 라이브러리 없음
- **단일 파일** — CSS·JS 인라인 포함

## 📝 라이선스

MIT
