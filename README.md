### README.md for IoT 구간별 교통체증 감시 시스템

---

# IoT 구간별 교통체증 감시 시스템

이 프로젝트는 IoT 기술을 이용하여 실시간 교통체증 감시 시스템을 구현한 것입니다. 이 시스템은 다양한 도로 구간에서 교통 데이터를 수집, 처리하여 사용자에게 실시간 교통 정보를 제공합니다.

## 목차

- [소개](#소개)
- [프로젝트 구조](#프로젝트-구조)
- [설치](#설치)
- [사용법](#사용법)
- [기능](#기능)
- [사용된 기술](#사용된-기술)
- [기여 방법](#기여-방법)
- [라이선스](#라이선스)

## 소개

이 프로젝트는 IoT 기술을 활용하여 국내 도로별 교통 정보를 실시간으로 수집하고, 구간별 교통 정보를 제공하는 시스템입니다. 이를 통해 교통 혼잡을 줄이고 운전자들에게 더욱 효율적인 교통 정보를 제공하는 것을 목표로 합니다.

## 프로젝트 구조

본 프로젝트는 실시간 교통 정보를 수집, 처리, 저장, 시각화하는 시스템으로 구성되어 있습니다. 주요 구성 요소는 다음과 같습니다:
1. **데이터 수집**: 한국 도로공사에서 제공하는 실시간 고속도로 정체 상황 API를 통해 교통 데이터를 수집합니다.
2. **MQTT 발행**: 수집된 데이터를 MQTT 메시지로 변환하여 발행합니다.
3. **Broker 서버**: Mosquitto를 사용하여 MQTT Broker 서버를 운영합니다.
4. **데이터 구독 및 저장**: Node.js를 활용하여 데이터를 구독하고 MongoDB에 저장합니다.
5. **데이터 제공 및 시각화**: 웹페이지를 통해 사용자에게 실시간 교통 정보를 시각적으로 제공합니다.

## 설치

```bash
# 레포지토리 클론
git clone https://github.com/yourusername/IoT-traffic-monitoring.git

# 프로젝트 디렉토리로 이동
cd IoT-traffic-monitoring

# 필요한 패키지 설치
npm install
```
## 사용법

1. **MQTT Broker 실행**: Mosquitto를 설치하고 MQTT Broker를 실행합니다.
2. **서버 실행**: Node.js 서버를 실행하여 데이터를 수집하고 저장합니다.
3. **웹페이지 접속**: 브라우저를 통해 웹페이지에 접속하여 실시간 교통 정보를 확인합니다.

```bash
# 서버 실행
node server.js
```

## 기능

- **실시간 교통 정보 수집 및 제공**: 한국 도로공사 API를 통해 실시간으로 교통 데이터를 수집하고, 이를 사용자에게 제공합니다.
- **표 및 차트 형태로 데이터 시각화**: 수집된 데이터를 표와 차트 형태로 시각화하여 사용자가 쉽게 이해할 수 있도록 합니다.
- **검색 기능**: 도로 이름을 검색하여 특정 도로의 교통 상태를 확인할 수 있습니다.
- **실시간 데이터 업데이트**: 실시간으로 데이터를 업데이트하여 최신 교통 정보를 사용자에게 제공합니다.
- **차트 타입 변경**: 사용자가 버튼을 클릭하여 차트 타입을 변경할 수 있는 기능을 제공합니다.
- **시간 위젯**: 현재 시간에 따른 교통량 변화를 확인할 수 있는 시계 위젯을 제공합니다.

## 사용된 기술

- **프로그래밍 언어**: Java, JavaScript
- **서버**: Node.js
- **데이터베이스**: MongoDB
- **MQTT Broker**: Mosquitto
- **라이브러리**: Socket.io, Chart.js

