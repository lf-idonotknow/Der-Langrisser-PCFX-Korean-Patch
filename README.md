# 데어 랑그릿사 FX 한국어 패치 v0.8.0

PC-FX판 《데어 랑그릿사 FX》의 비공식 한국어 패치입니다. 게임 내 대사와 메뉴를 한글화하고, 동영상에 한국어 자막을 제공합니다.

## 다운로드

[v0.8.0 패치 ZIP](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/releases/download/v0.8.0/Der-Langrisser-PCFX-Korean-Patch-v0.8.0.zip)을 내려받으십시오. GitHub의 `Source code` ZIP에는 적용에 필요한 패치 데이터가 들어 있지 않습니다.

## 한글화 내용

- 본편 대사와 선택지
- 시나리오 소개와 캐릭터 후일담
- 인명·클래스·병종·아이템·마법
- 각종 메뉴와 정보창
- 동영상 한국어 자막

음성은 일본어 원음을 유지합니다. 일부 이미지에 포함된 일본어는 남아 있습니다.

## 검수 범위

**Android용 RetroArch에서 빛의 후예 시나리오를 엔딩까지 직접 플레이하며 검수했습니다.**

다른 분기와 모든 후일담 조합의 검수는 아직 완료되지 않았습니다.

## 준비물

- PC-FX 일본판 원본 `Der Langrisser FX.bin`
- 원본 `Der Langrisser FX.cue`
- Python 3.9 이상
- xdelta3

원본 게임과 BIOS는 제공하지 않습니다. xdelta3는 [공식 프로젝트](https://github.com/jmacd/xdelta)에서 별도로 준비해 주십시오.

## 지원 원본

다음 BIN과 정확히 일치하는 PC-FX 일본판 원본이 필요합니다. 파일 이름이 같더라도 크기나 SHA-256이 다르면 적용할 수 없습니다.

- 파일: `Der Langrisser FX.bin`
- 크기: 775,880,112바이트
- SHA-256: `a1a2a501400bc5d9b3a06ba4600e4e7dee686974c089916c2b8f9ff7abb7cb73`

원본 BIN과 함께 사용하는 원본 `Der Langrisser FX.cue`도 필요합니다.

## 적용 방법

1. 패치 ZIP을 내려받아 압축을 풉니다.
2. 동봉된 `README_KO.md`에 따라 원본 BIN과 CUE를 지정하여 적용기를 실행합니다.
3. 적용이 끝나면 생성된 한국어판 CUE 파일을 에뮬레이터에서 실행합니다.

패치는 지원 원본에 적용합니다. 원본 파일은 변경하지 않으며, 한국어판 파일을 별도의 폴더에 생성합니다.

출력 폴더는 적용 전에 존재하지 않는 새 경로를 지정해 주십시오. 적용에는 약 1GB의 여유 공간이 필요합니다.

동봉 적용기가 원본과 적용 결과의 크기 및 SHA-256을 자동으로 확인합니다.

## 패치 적용 결과

정상적으로 적용되면 다음 파일이 생성됩니다.

- `Der Langrisser FX Korean.bin`
- `Der Langrisser FX Korean.cue`

결과 BIN:

- 크기: 778,669,584바이트
- SHA-256: `e3a31e66bbd6ca02a0f3aedc4008c2917f94b9d76e3674daba708735a4c3ef99`

에뮬레이터에서는 **`Der Langrisser FX Korean.cue`**를 실행하십시오. 원본 CUE를 한국어판 BIN에 재사용하지 마십시오.

Android 기기로 옮길 때는 생성된 BIN과 CUE를 같은 폴더에 넣고, RetroArch에서 CUE를 선택하십시오.

## 오류 제보

문제가 발생하면 [Issues](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/issues)에 다음 내용을 함께 알려 주십시오.

- 패치 버전
- 사용한 에뮬레이터 이름과 버전
- 발생한 시나리오와 장면
- 문제 직전에 수행한 조작
- 문제 화면

ROM·BIOS 파일이나 계정 정보는 첨부하지 마십시오.

## 저작권과 배포

게임 및 원작의 저작권은 각 권리자에게 있습니다. 이 패치는 팬이 제작한 비공식 번역 패치이며, 원본 또는 패치된 전체 디스크 이미지를 포함하지 않습니다.

글꼴과 제3자 구성요소의 출처 및 라이선스는 [CREDITS.md](CREDITS.md), [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md), [OFL-1.1.txt](OFL-1.1.txt)를 확인해 주십시오.
