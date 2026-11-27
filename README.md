<p align="center">
  <img width="100" height="100" alt="Tracer_icon" src="https://github.com/user-attachments/assets/22ebe517-6be2-4dd7-ae8e-e2f241f120b7" />

</p>

<h1 align="center">Tracer v1.0.0</h1>

<p align="center">
  RF Impedance Matching, Smith Chart &amp; Component SOA Tool for Windows<br/>
  <a href="#english">English</a> &nbsp;|&nbsp; <a href="#한국어">한국어</a> &nbsp;|&nbsp; <a href="https://github.com/T-ReF/Tracer/releases">Download (Releases)</a>
</p>

---

<a id="english"></a>

## English

**Tracer** is a desktop RF engineering tool built for day-to-day impedance matching, Smith Chart work, and component stress checks — mainly around 13.56 MHz RF / plasma matching networks, though it works at any frequency.

I built it because checking variable vacuum capacitor (VVC) voltage/current ratings, tuning ranges, and S11/power response across a matching network usually meant jumping between spreadsheets, VNA software, and heavy simulators. Tracer puts those pieces in one fast native desktop app.

<!-- Tip: In GitHub's README editor, you can drag and drop your app screenshots right here -->
<p align="center">
</p>
<img width="960" height="520" alt="image" src="https://github.com/user-attachments/assets/8755f6ea-90f8-41dd-b4b5-f70800bd378c" />

### Download & Run

Grab the latest Windows build from the [**Releases**](https://github.com/T-ReF/Tracer/releases) page.

- **Installer (`Tracer_v1.0.0_Setup.exe`)** — standard Windows installer.
- **Portable (`Tracer_v1.0.0_Portable.zip`)** — unzip anywhere and run `Tracer_v100.exe`. No Python installation required.

> Tested on Windows 10 / 11 (64-bit). Because the binary is not code-signed yet, Windows SmartScreen may show a warning on first launch — click *More info → Run anyway*.

### Main Features

- **Circuit Builder & Interactive Smith Chart**
  - Build series/shunt R, L, C, VVC, transformer, and compound stages (`p-L+VC`, `s-VC||C`, `p-VC||C`) with L / T / Pi presets.
  - Built-in Comet and Meidensha vacuum capacitor presets (C_min~C_max, working peak voltage, RMS current).
  - Fast 2D tuning range calculation (up to 500×500 points) with Best Match search and one-click apply.
  - Live on-schematic voltage/current stress HUD for both current state and best match.

- **Data Export**
  - Export Tuning Range and SOA results to multi-sheet **Excel (`.xlsx`)** or **CSV (`.csv`)** sets (`UTF-8-SIG`, `#` comment metadata ready for Excel, Python/pandas, or MATLAB).
  - Load and export Touchstone (`.s1p`) traces and matchable region clouds.

- **Extra Utilities**
  - RF filter design, coaxial/transmission line calculator, impedance conversion utilities, plasma/vacuum calculators, and VNA/oscilloscope capture helpers.

### Feedback

If you run into a bug, notice a calculation discrepancy, or want a capacitor preset added, please open an [Issue](https://github.com/T-ReF/Tracer/issues).

---

<a id="한국어"></a>

## 한국어

**Tracer**는 RF 임피던스 매칭, 스미스 차트 해석, 소자 내압/전류 스트레스(SOA) 검토를 한 화면에서 빠르게 하기 위해 만든 Windows 데스크톱 프로그램입니다. 주로 13.56 MHz 플라즈마 매칭 네트워크 설계를 염두에 두고 만들었지만, 일반 RF 주파수 대역에서도 그대로 사용할 수 있습니다.

현장에서 매칭 회로를 잡다 보면 VVC(진공 가변 커패시터) 내압·전류 여유, 튜닝 영역, S11/반사전력 등을 엑셀과 시뮬레이터를 오가며 확인해야 하는 번거로움이 있는데, 자주 쓰는 계산과 스미스 차트 시각화를 가볍게 한곳에 모아두었습니다.

<p align="center">
  <img src="assets/screenshot_soa.png" alt="Tracer SOA Power Limit" width="92%" />
</p>

### 다운로드 및 실행

[**Releases**](https://github.com/T-ReF/Tracer/releases) 페이지에서 최신 Windows 실행 파일을 받을 수 있습니다.

- **설치 버전 (`Tracer_v1.0.0_Setup.exe`)** — 일반 Windows 설치 파일
- **포터블 버전 (`Tracer_v1.0.0_Portable.zip`)** — 압축 해제 후 `Tracer_v100.exe` 바로 실행 (별도 Python 설치 불필요)

> Windows 10 / 11 (64-bit) 환경에서 테스트했습니다. 코드 서명이 없는 개인 빌드라 첫 실행 시 Windows SmartScreen 경고가 뜰 수 있으며, *추가 정보 → 실행*을 누르시면 됩니다.

### 주요 기능

- **Circuit Builder & 스미스 차트**
  - 직렬/병렬 R, L, C, VVC, 트랜스포머 및 복합 소자(`p-L+VC`, `s-VC||C`, `p-VC||C`) 구성, L / T / Pi 토폴로지 프리셋 지원.
  - Comet / Meidensha 주요 진공 가변·고정 커패시터 프리셋 내장 (용량 범위, 정격 피크 전압, RMS 전류).
  - 2D 튜닝 영역(최대 500×500 포인트) 고속 계산, Best Match 자동 탐색 및 원클릭 적용.
  - 회로도 위에서 각 단의 전압·전류 스트레스를 바로 확인하는 HUD 오버레이.

- **데이터 내보내기**
  - Tuning Range / Frequency Sweep / SOA 결과를 멀티 시트 **Excel(`.xlsx`)** 또는 **CSV(`.csv`)** 세트로 저장 (`UTF-8-SIG`, `#` 메타데이터 주석 지원).
  - Touchstone(`.s1p`) 파일 불러오기 및 매칭 영역 클라우드 내보내기.

- **기타 도구**
  - RF 필터 설계, 동축/전송선로 계산기, 임피던스 변환 도구, 플라즈마·진공 계산기, VNA/오실로스코프 연동 기능.

### 문의 및 피드백

버그나 계산 오차, 추가했으면 하는 커패시터 프리셋이 있으면 [Issues](https://github.com/T-ReF/Tracer/issues)에 남겨주세요.

---

<p align="center">
  <sub>Built by <a href="https://github.com/T-ReF">T-ReF</a></sub>
</p>
