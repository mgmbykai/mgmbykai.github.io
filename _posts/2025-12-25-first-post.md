---
title: "[Dev] 한국투자증권 KIS Developers Open API 핵심 리소스 정리"
excerpt: "효율적인 자동매매 프로그램 개발을 위한 한국투자증권 API 필수 링크 가이드"
categories:
  - Finance
tags:
  - KIS
  - Stock
  - API
  - Python
last_modified_at: 2025-12-25T22:40:00+09:00
toc: true
toc_sticky: true
toc_label: "Quick Links"
---

## 🏛️ KIS Developers Ecosystem

한국투자증권의 **Open API**는 국내 및 해외 주식, 파생상품 매매를 위한 강력한 인터페이스를 제공합니다. 성공적인 알고리즘 매매의 첫걸음은 정확한 문서 확인에서 시작됩니다.

---

### 📘 Official Documentation
> 최신 명세서와 가이드가 담긴 공식 포털입니다.

* [**KIS Developers 공식 포털**](https://apiportal.koreainvestment.com/) : 메인 페이지 및 공지사항 확인
* [**API 상세 명세서 (Wiki)**](https://apiportal.koreainvestment.com/help/itp) : 각 기능별 호출 주소 및 파라미터 상세 안내
* [**모의투자 신청 가이드**](https://apiportal.koreainvestment.com/help/customer-service?id=6) : 실전 매매 전 테스트를 위한 필수 코스

---

### 💻 Developer Resources
> 개발 속도를 높여주는 라이브러리와 예제 코드 저장소입니다.

| 구분 | 리소스 링크 | 비고 |
| :--- | :--- | :--- |
| **Github Repo** | [**KIS 공식 샘플 코드**](https://github.com/koreainvestment/open-api-korea) | Python/Java/C# 예제 제공 |
| **Python SDK** | [**mohid-kis (Unofficial)**](https://pypi.org/project/mohid-kis/) | 더 간결한 래퍼 라이브러리 |
| **Community** | [**개발자 포럼 (Q&A)**](https://apiportal.koreainvestment.com/community/forum) | 에러 코드 및 문제 해결 공유 |

---

### 🛠️ Essential Endpoints
자동 매매 봇 개발 시 가장 빈번하게 참조하게 될 핵심 API 엔드포인트입니다.

#### 1. 인증 및 보안
* [**접근 토큰(P_AUTH) 발급**](https://apiportal.koreainvestment.com/help/itp?id=1)
* [**Hashkey 생성**](https://apiportal.koreainvestment.com/help/itp?id=2)

#### 2. 국내 주식 주문
* [**주식주문(현금)**](https://apiportal.koreainvestment.com/help/itp?id=30)
* [**주식주문(정정/취소)**](https://apiportal.koreainvestment.com/help/itp?id=32)

#### 3. 시세 및 잔고
* [**주식 현재가 시세**](https://apiportal.koreainvestment.com/help/itp?id=45)
* [**주식 잔고 조회**](https://apiportal.koreainvestment.com/help/itp?id=124)

---

### 💡 Development Tips
1.  **초당 호출 제한(Throttle)**: 실전 API는 초당 호출 횟수 제한이 엄격하므로 `time.sleep()` 또는 비동기 처리가 필수입니다.
2.  **WebSocket 활성화**: 실시간 시세는 HTTP 호출보다 WebSocket을 통한 수신이 훨씬 효율적입니다.
3.  **에러 핸들링**: `RT_CD`가 `0`이 아닌 경우의 예외 처리를 꼼꼼하게 설계하세요.

---

> **Note**: 한국투자증권 API는 정기 점검 시간(보통 00:00 ~ 01:00) 동안 접속이 제한될 수 있습니다.