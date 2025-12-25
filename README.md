# 📈 AlgoTrade-KR: Stock & Crypto Auto-Trading Bot

<p align="center">
  <img src="https://img.shields.io/badge/python-3.12-blue?logo=python&logoColor=white" alt="Python Version">
  <img src="https://img.shields.io/endpoint?url=https://atp-stats.herokuapp.com/v1/projects/astral-sh/uv" alt="uv Package Manager">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

---

### 🚀 Overview
**AlgoTrade-KR**은 한국투자증권(KIS)과 업비트(Upbit) API를 통합하여 주식과 가상자산을 한곳에서 관리하고 자동 매매하는 오픈소스 프로젝트입니다. 최신 파이썬 패키지 매니저인 `uv`를 채택하여 번개처럼 빠른 환경 구축과 안정적인 실행을 지원합니다.

---

## ✨ Key Features

* **Dual-Market Integration**: 국내 주식과 암호화폐 시장을 하나의 로직으로 제어.
* **Next-Gen Environment**: `uv`를 통한 초고속 패키지 관리 및 가상환경 격리.
* **Real-time Analysis**: WebSocket을 이용한 실시간 시세 데이터 수집 및 기술적 지표 계산.
* **Smart Strategy Engine**: 
    * 변동성 돌파 전략 (Larry Williams Volatility Breakout)
    * RSI 및 볼린저 밴드 기반 역추세 매매
    * 커스텀 전략 손쉬운 추가 기능
* **Instant Notifications**: 매매 발생 시 Telegram/Slack 실시간 알림 전송.

---

## 🛠 Tech Stack

| 분류 | 기술 스택 |
| :--- | :--- |
| **Language** | Python 3.12+ |
| **Package Manager** | `uv` (Fastest Python package manager) |
| **Stock API** | 한국투자증권 KIS Developers Open API |
| **Crypto API** | Upbit Open API |
| **Data Analysis** | Pandas, NumPy, TA-Lib |
| **Asynchronous** | `asyncio`, `aiohttp` |

---

## 📦 Getting Started

### 1. `uv` 설치 (미설치 시)
```bash
# Windows
powershell -c "ir.exe -useb [https://astral.sh/uv/install.ps1](https://astral.sh/uv/install.ps1) | iex"
# macOS/Linux
curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh