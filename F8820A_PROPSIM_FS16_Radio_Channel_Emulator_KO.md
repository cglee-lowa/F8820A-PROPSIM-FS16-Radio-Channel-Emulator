# F8820A PROPSIM FS16 무선 채널 에뮬레이터 (데이터시트 한국어 번역·요약본)

> 원본: Keysight F8820A PROPSIM FS16 Data Sheet (2025-05-15, 3119-1108.EN)
> 본 문서는 원문 데이터시트의 한국어 번역·요약본이며, 홍보성 문구는 생략하고 기술 사양 중심으로 정리했습니다. 정확한 값은 반드시 원문 PDF(`F8820A_PROPSIM_FS16_Radio_Channel_Emulator.pdf`)를 기준으로 확인하세요.

## 개요

PROPSIM FS16은 송신기와 수신기 사이의 동적 무선 채널을 실시간으로 에뮬레이션합니다. 5G, 4G, 항공우주, 방산 분야 무선 시험에 필요한 단방향/양방향 페이딩 테스트 구성을 경제적으로 지원합니다. 단일 장비에서 2~256개, 다중 장비 구성에서 최대 1024개의 페이딩 채널을 지원합니다. 이보다 큰 페이딩 용량이 필요하면 PROPSIM F64를 사용합니다.

FR1/FR2 대역의 5G NR MIMO 및 MIMO OTA 페이딩 시험에 적합한 소형·저비용 제품이며, Keysight 네트워크 에뮬레이션 및 mmWave OTA 시험 솔루션과 연동됩니다.

**주요 시험 대상**
- 5G, LTE-A 및 기존 기술을 지원하는 단말과 기지국
- WLAN 802.11ax 액세스 포인트 및 단말
- 전술 MANET/메시 무선 시스템
- 항공우주 및 5G NTN 위성 무선 시스템
- 지상·항공·위성 혼합 무선 시스템

RF 범위는 3 MHz ~ 53 GHz이며 초광대역 순시 신호 대역폭을 지원합니다.

## 정의 및 조건

다음 조건에서 사양을 만족합니다.
- 하드웨어가 교정 주기 이내일 것
- 허용 보관 온도 범위 안이지만 동작 온도 범위 밖에 보관되었던 경우, 동작 온도 환경에서 전원 투입 전 최소 6시간 보관할 것
- 시험 장비를 최소 60분간 켜 둘 것
- PROPSIM 내장 PC(Windows)에서 PROPSIM 실행 화면 외에 다른 애플리케이션이나 서드파티 소프트웨어를 동시에 실행하지 않을 것

**용어**
- **사양(Specification)**: 제품 보증 대상 성능 파라미터. 별도 표기가 없으면 15~30 °C에서 유효.
- **전형값(Typical)**: 보증 대상이 아닌 추가 성능 정보. 95 % 신뢰수준에서 95 %의 제품이 만족하는 성능이며 측정 불확도는 제외, 23 °C 실온에서만 유효.
- **공칭값(Nominal)**: 예상 성능 또는 활용에 유용한 참고 값으로 보증 대상 아님.

## 주요 기능 및 구성

| 항목 | 내용 |
|---|---|
| 단일 장비 RF 포트 | 소프트웨어 설정으로 최대 16개 양방향 TRX 포트 또는 16개 단방향 TX/RX 포트. 모든 포트 SMA 암(female) 커넥터. 출하 구성: 2(F8820AC02), 4(C04), 8(C08), 12(C12), 16(C16) (T)RX+TX 포트 |
| MIMO 페이딩 채널 | 양방향/단방향 페이딩 지원. 단일 장비 최대 256 디지털 채널(16x16), 다중 장비(4대) 최대 1024 페이딩 채널. 임의의 MIMO 및 멀티링크 토폴로지 지원. ※ TRX 포트, RFLO, 디지털 페이딩 채널의 조합이 매우 복잡하면 기저대역 데이터 라우팅 한계로 지원되지 않을 수 있으므로, 반드시 PROPSIM 에뮬레이터 및 Standard Tools 소프트웨어로 구성 가능 여부를 확인해야 함 |
| MIMO / Massive MIMO | 단일 장비: 최대 8x8 양방향 또는 16x16 단방향 MIMO, MIMO OTA 2x16/4x16/8x16. 다중 장비: 외부 안테나 인터페이스 유닛 또는 RF 위상천이기 매트릭스를 이용한 단순화된 안테나 어레이 샘플링 Massive MIMO 시험 |
| MESH / MANET 에뮬레이션 | 단일 장비에서 최대 16개 무선기 풀 메시. 최대 무선기 수는 대역폭과 채널 모델 특성에 따라 달라지며, 복잡한 구성은 지원되지 않을 수 있어 사전 확인 필요 |
| 주파수 범위 | Opt-R30: 450~3000 MHz / Opt-R60: 450~6000 MHz / Opt-R04: 3~450 MHz(R30 또는 R60 필요, 3 MHz는 RF 범위 가장자리). M1742A 사용 시 10~32 GHz, M1740A 사용 시 24.25~29.5 GHz 및 37~43.5 GHz, M1749B 사용 시 24.5~53 GHz (모두 Opt-R60 필요). F882SATxA 동작은 140 MHz 이상에서 지원 |
| 연결 방식 | RF 유선 연결, OTA 챔버 |
| 순시 신호 대역폭 | Opt-040: 40 MHz / Opt-010: 100 MHz / Opt-016: 160 MHz (각각 최대 16 TRX 채널) |
| 확장 대역폭 옵션 (450 MHz 이상에서 규정) | Opt-EX1: 300 MHz(최대 8 TRX) / EX2: 450 MHz(최대 4) / EX3: 600 MHz(최대 4) / EX4: 900 MHz(최대 2) / EX5: 1200 MHz(최대 2). F880SATxA와 함께 사용 시 정밀한 응답 보정을 위해 외부 VNA 필요 |
| 캐리어 어그리게이션 | 연속 최대 1200 MHz (TDD/FDD), 비연속 최대 8개 CA 대역 |
| 독립 RF 로컬 오실레이터 | 단일 F8820A에서 최대 8개 |
| 주파수 변환 (예: 대역 A → B) | 지원, 최소 RFLO 2개 필요 |
| 450 MHz 이상 RF 대역 내부 결합 | 단일 RF TRX 포트로 최대 8개 RF 대역 |
| 페이딩 채널당 페이딩 경로 | 최대 48 |
| 최소 지연 | 2 μs 미만 (MIMO 단일 채널 유닛 토폴로지, 100/160 MHz BW) |
| 최대 지연 | 기본 335 μs. -ED1 옵션: 1500 ms(항공우주 에뮬레이션 모드), -ED2 옵션: 100 ms(지상 장지연). 해당 옵션 활성 시 TRX 채널당 디지털 채널 1개 지원 |
| 도플러 에뮬레이션 | 최대 ±1.5 MHz, F880SATxA 옵션 필요 |
| 시험 환경 교정 | 진폭·위상 교정 통합. 루프백 연결 기반 위상/진폭 정렬(110 MHz 이상), 외부 VNA를 이용한 자동 응답 보정, 3GPP NR/LTE DL 신호 기반 입력 위상 정렬 |
| 간섭원 | **CW**: 출력 포트별 독립 비상관 소스, 주파수 오프셋 조정, 절대값/SNR 기반 레벨 설정. **AWGN**: 포트별 독립 비상관 소스, 사용자 지정 대역폭·주파수 오프셋, 절대값/SNR 레벨. **임의 파형 간섭**: PathWave Signal Generation으로 생성한 파형 사용, 간섭원 분배/결합 및 페이딩 적용 가능, 표준 기반/사용자 정의 변조, 버스트, 변조 펄스, 처프 등 지원 |
| 입력 레벨 자동 설정 | 연속 및 RF 버스트 모드 |
| 상·하향링크 분리 | 통합 지원 |
| 입출력 포트 | 사용자 정의 활성 커넥터 설정 |
| 기타 인터페이스 | 10 MHz 기준 입·출력, 에뮬레이션 시작/정지용 HW 트리거 포트, 다중 장비 동기 포트 |

## PROPSIM 소프트웨어 및 채널 모델

- **Standard Tools**: FR1/FR2용 3GPP 5G NR TDL 채널 모델, LTE, WCDMA, GSM, Static Butler
- **Channel Studio GCM Tool**: 3GPP TR38.901, TR36.873, WINNER, SCME / 레이트레이싱 데이터 가져오기 / 3D 안테나 패턴 포함 / Massive MIMO, D2D, V2X용 사용자 정의 시험 토폴로지 / MIMO OTA 채널 모델(CTIA/3GPP/CCSA)
- **Channel Studio NTN Tool**: 위성 시나리오 및 3GPP TR38.811 기반 NTN 모델
- **Channel Studio WLAN Tool**: 802.11ax/be 채널 모델
- **Channel Studio RF Field-to-Lab Tool**: 5G 및 LTE용
- **고속열차(High-Speed Train) 채널 모델 팩** (이동통신사업자 시험 계획 기반)
- **고속 페이딩 프로파일**: Constant, Rayleigh, Rice, Nakagami, Lognormal, Suzuki, Pure Doppler, flat, rounded, Gaussian, Jakes, Butterworth, 사용자 정의, 서드파티 시뮬레이션 도구의 CIR 데이터. 디지털 채널마다 지연·도플러·진폭·상관을 독립 설정 가능
- **경로손실/섀도잉** (섀도잉 옵션 사용 시): TRX 채널별 독립, 동적 범위 100 dB / 디지털 페이딩 채널별 독립, 동적 범위 60 dB
- **지연 프로파일**: Constant, sliding delay, 3GPP birth-death, 3GPP sliding delay group, 사용자 정의, 서드파티 시뮬레이션 도구 및 레이트레이싱 애플리케이션. 디지털 페이딩 채널마다 독립 지연 설정

## RF 특성 (F8820A, 3 MHz ~ 6 GHz, 160 MHz BW 신호 기준)

| 항목 | 값 |
|---|---|
| RF 입력 레벨 | +35 dBm(피크), 100 MHz 미만에서는 +15 dBm(피크) |
| RF 출력 레벨 | TRX 포트 +5 dBm(피크), TX 포트 +15 dBm(피크) |
| RF 입출력 분해능 | 0.1 dB |
| 출력 게인 설정 범위 | TRX 포트 +5 ~ -100 dB, TX 포트 +15 ~ -100 dB |
| 출력 레벨 정확도 | 중심 주파수에서 ±0.5 dB 미만 (전형값) |
| 출력 잡음 바닥 | -170 dBm/Hz 미만 (출력 ≤ -40 dBm, 전형값), 30 MHz 미만에서 -160 dBm/Hz 미만 |
| 잔류 EVM | 5G NR 100 MHz, 1024QAM, 3.5 GHz에서 -48 dB RMS 미만(전형값) / 802.11ax 160 MHz, 1024QAM, 5.815 GHz에서 -45 dB RMS 미만(전형값). 잔류 EVM은 PROPSIM이 입력 신호에 추가하는 EVM 기여분. 802.11ax 측정 설정: 데이터 OFDM 심볼 16개, 파일럿만으로 위상 추적, EQ 학습은 프리앰블만, 채널 추정 필터 Wiener(DS 0.001) |
| TRX/TX 포트 간 누화 | -100 dB 미만 (전형값) |
| 전 RF 포트 VSWR (공칭) | 3~700 MHz: 1.8 미만 / 700 MHz~2 GHz: 1.3 미만 / 2~6 GHz: 1.5 미만 |

## 신호 캡처 및 재생 (해당 구성 및 옵션 필요)

| 항목 | 내용 |
|---|---|
| 신호 캡처 | 위상 동기 동시 캡처 최대 16개 (F8800A-ME1 옵션 시 64개). 파일 형식: Keysight PathWave 89600 VSA, WaveJudge Wireless Analyzer, 개방형 포맷. 최대 순시 BW 160 MHz. 옵션 설치는 Keysight 서비스 센터에서 수행 |
| 캡처 트리거 | GUI / SCPI / LVTTL(BNC) 단일 트리거, 트리거 지연 ±1000 ms 조정, 에뮬레이션 시간 기준 |
| 신호 파형 재생 | 위상 동기 소스 최대 16개 (F8800A-ME1 시 64개). Keysight PathWave Signal Generation 파형 지원. 최대 순시 BW 160 MHz. 옵션 설치는 Keysight 서비스 센터에서 수행 |
| 재생 트리거 | GUI / SCPI / LVTTL(BNC) 단일 트리거, 트리거 지연 5 μs ~ 1000 ms |
| 재생·캡처 메모리 | RF 포트당 1000 ms (BW 100/160 MHz) |

## 장비 사양

| 항목 | 내용 |
|---|---|
| 원격 제어 | 이더넷 ATE SCPI 명령, Keysight Test Automation on PathWave(TAP)용 PROPSIM 플러그인 |
| 타임베이스 | 표준 주파수 기준 10 MHz(공칭), 최대 주파수 드리프트 ±0.1 ppm/2년, 워밍업 30분 |
| 동기화 | 에뮬레이션 시작/정지 HW 트리거 포트, 다중 PROPSIM 하드웨어 동기 포트. 동일 네트워크 시간 기준을 쓰는 다른 장비와 에뮬레이션을 동기 시작하는 UTC 시간 트리거(NTP로 시스템 시간 보정, 모든 타임스탬프에 보정 시간 사용). 낮은 stratum NTP 서버 사용 시 UTC 동기 정밀도 20 ms 미만(전형값) |
| 기타 인터페이스 | 10 MHz 기준 입·출력, LAN 1 Gbps, USB 6개, DisplayPort 2개 |
| 전압/주파수 | 2 x 200~240 VAC, 50/60 Hz |
| 소비 전력 | FS16-8 TRX: 800 W / FS16-16 TRX: 1200 W |
| 소비 전류 | 1 x 15 A 최대 |
| 외형 치수 (H x W x D) | 290 mm x 435 mm x 600 mm, 19인치 랙 장착 가능 |

상세 제품 구성 항목, 필요 옵션, 가격 및 지원 서비스는 영업 담당자에게 문의하세요.

## Keysight 5G 솔루션 및 참고 링크

Keysight는 시뮬레이션·설계·검증부터 제조·배치·최적화까지 5G 제품 개발 전 과정을 위한 엔드투엔드 설계·시험 솔루션을 제공하며, 최신 3GPP 표준을 따르는 공통 소프트웨어·하드웨어 플랫폼으로 5G 칩셋, 단말, 기지국, 네트워크를 검증합니다.

- 5G 솔루션: www.keysight.com/find/5G
- PROPSIM 채널 에뮬레이션: http://www.keysight.com/find/PROPSIM
- F8820B PROPSIM FS16: https://www.keysight.com/product/F8820B/
- PROPSIM 플랫폼: https://www.keysight.com/us/en/products/channel-emulators/propsim-platforms.html
- PathWave: http://www.keysight.com/find/pathwave
- M1740A mmWave 트랜시버: http://www.keysight.com/find/m1740a
- M1742A 트랜시버(10~32 GHz) / M1749B 트랜시버(24~53 GHz): https://www.keysight.com/us/en/product/M1749B

---
© Keysight Technologies, 2022–2025. 본 정보는 예고 없이 변경될 수 있습니다. (원문 발행: 2025-05-15, 문서 번호 3119-1108.EN)
