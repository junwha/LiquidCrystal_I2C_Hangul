# LiquidCrystal_I2C_Hangul : LCD 한글 출력 라이브러리

이 라이브러리는 I2C 통신을 사용하는 16x2 또는 20x4 LCD에서 한글을 출력할 수 있는 라이브러리입니다. 

This library enables printing Hangul (Korean) on 16x2 or 20x4 LCDs using I2C communication.

# 라이브러리 사용법 (Getting Started)

###  Arduino 라이브러리 매니저에서 설치

Arduino IDE -> 스케치(Sketch) -> 라이브러리 포함하기(Include Library) -> 라이브러리 관리(Library Manager)에서 'LiquidCrystal_I2C_Hangul'을 검색하여 간편하게 설치할 수 있습니다.

### GitHub에서 ZIP 파일 다운로드 후 설치

본 저장소의 좌측 하단 Releases 페이지에서 최신 Release를 다운로드합니다.

Arduino IDE에서 스케치(Sketch) → 라이브러리 포함하기(Include Library) → .ZIP 라이브러리 추가(Add .ZIP Library) 메뉴를 통해 라이브러리를 추가하세요.

# API Documentation

## 표준 API

이 라이브러리는 기존 [LiquidCrystal_I2C](https://docs.arduino.cc/libraries/liquidcrystal-i2c/) 라이브러리에 포함된 모든 함수를 지원합니다.

## 한글 출력 전용 API

한글 출력을 위해 다음과 같은 추가적인 기능을 제공합니다:

### `printHangul(wchar_t* txt, byte firstPoint, byte len)`

- 첫 번째 인자로 wchar_t 타입의 한글 문자열을 입력합니다.

- 두 번째 인자는 글자가 시작하는 위치(0~15)를 지정합니다.

- 세 번째 인자는 출력할 글자의 길이입니다.

- 주의사항:

   - 공백 문자 및 특수문자는 지원되지 않습니다. 일반 문자열 출력에는 print() 함수를 사용하세요.

   - 'ㅡ' 형 문자는 좌우 1칸을, 'ㅣ' 형 문자는 좌우 2칸을 차지합니다.

### `setDelayTime(int t)`

- 글자가 출력되는 속도를 설정할 수 있습니다. (기본값: 1000ms)


# Contributors

Junwha Hong @junwha

Dohun Kim @uthem150

Perl @per1234

