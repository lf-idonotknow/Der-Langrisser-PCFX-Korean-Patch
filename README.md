# 데어 랑그릿사 FX 한국어 패치 v0.8.1

PC-FX판 《데어 랑그릿사 FX》의 비공식 한국어 패치입니다. 게임 내 대사와 메뉴를 한글화하고, 동영상에 한국어 자막을 제공합니다.

[패치 ZIP 다운로드](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/releases/download/v0.8.1/Der-Langrisser-PCFX-Korean-Patch-v0.8.1.zip)

## 이번 업데이트

- 타이틀 화면의 로고를 `데어 랑그릿사 FX`로 한글화했습니다.
- 시작 메뉴를 `시작 / 불러오기`로 한글화했습니다.
- 오프닝 동영상 마지막의 로고도 한글화하고, 정지 타이틀로 넘어갈 때 위치가 어긋나지 않도록 맞췄습니다.
- 기존 대사·메뉴·동영상 자막·후일담 한글화는 유지됩니다.

**기존 버전을 사용하셨더라도, 한글판에 덧씌우지 말고 미패치 일본판 원본 BIN에 이번 패치를 적용하십시오. CUE도 이번 ZIP에 들어 있는 파일로 교체해야 합니다.**

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
- xdelta 패처(xdelta UI 또는 Delta Patcher)
- 약 1GB의 출력 공간

**일반 xdelta 패처로 적용할 수 있으며 Python은 필요하지 않습니다.** 이미 쓰고 계신 xdelta UI가 있으면 그대로 사용하시면 됩니다.

패처가 없다면 [Delta Patcher 공식 다운로드](https://github.com/marco-calautti/DeltaPatcher/releases/latest)에서 운영체제에 맞는 파일을 받으십시오. 일반 Windows PC는 `windows_bin_x86_64.zip`을 풀고 `DeltaPatcher.exe`를 실행하면 됩니다. Delta Patcher에는 xdelta 기능이 포함되어 있어 별도 `xdelta3.exe`가 필요하지 않습니다.

원본 게임과 BIOS는 제공하지 않습니다.

## 지원 원본

다음 BIN과 정확히 일치하는 PC-FX 일본판 원본이 필요합니다. 파일 이름이 같더라도 크기나 SHA-256이 다르면 적용할 수 없습니다.

- 파일: `Der Langrisser FX.bin`
- 크기: 775,880,112바이트
- SHA-256: `a1a2a501400bc5d9b3a06ba4600e4e7dee686974c089916c2b8f9ff7abb7cb73`

이미 한글 패치를 적용한 BIN, CHD, 여러 트랙으로 나뉜 BIN에는 적용하지 마십시오.

## 적용 방법

패치 ZIP `Der-Langrisser-PCFX-Korean-Patch-v0.8.1.zip`을 내려받아 압축을 풉니다. GitHub의 `Source code` ZIP은 패치 파일이 아닙니다. 아래 두 방법 중 사용 중인 패처에 맞는 하나만 실행하십시오.

### xdelta UI를 사용하는 경우

1. xdelta UI의 **Apply Patch** 탭을 엽니다.
2. 다음과 같이 파일을 지정합니다.

| 항목 | 선택할 파일 |
|---|---|
| Patch | 압축을 푼 `Der-Langrisser-PCFX-Korean-Patch-v0.8.1.xdelta` |
| Source File | 본인이 보유한 원본 `Der Langrisser FX.bin` |
| Output File | 새 폴더 안의 `Der Langrisser FX Korean.bin` |

3. **Patch** 버튼을 누르고 완료될 때까지 기다립니다. 출력 경로는 원본 BIN과 다른 경로로 지정하십시오.
4. ZIP에 동봉된 **`Der Langrisser FX Korean.cue`**를 결과 BIN과 같은 폴더에 복사합니다.
5. 에뮬레이터에서 **`Der Langrisser FX Korean.cue`**를 엽니다.

### Delta Patcher를 사용하는 경우

1. 새 폴더를 만들고 원본 BIN을 **복사**한 뒤, 복사본 이름을 `Der Langrisser FX Korean.bin`으로 바꿉니다. Delta Patcher는 선택한 파일을 갱신하므로 반드시 복사본을 사용하십시오.
2. **Original file**에 방금 만든 `Der Langrisser FX Korean.bin` 복사본을 선택합니다.
3. **XDelta patch**에 `Der-Langrisser-PCFX-Korean-Patch-v0.8.1.xdelta`를 선택합니다.
4. **Apply patch**를 누르고 성공 메시지를 확인합니다. `Checksum validation`은 켜 둡니다.
5. 동봉된 `Der Langrisser FX Korean.cue`를 같은 폴더에 복사하고 에뮬레이터에서 이 CUE를 엽니다.

패치는 BIN에만 적용합니다. CUE에는 패치를 적용하지 않으며, **반드시 동봉된 한국어판 CUE**를 사용해야 합니다.

### CUE를 함께 써야 하는 이유

BIN은 게임 데이터이고, CUE는 그 데이터와 음악 트랙의 위치를 알려 주는 안내표입니다. 한글화 데이터를 추가하면서 뒤쪽 데이터와 음악 트랙의 시작 위치가 달라졌습니다. 원본이나 이전 버전 CUE를 쓰면 잘못된 위치를 읽어 게임이 시작되지 않거나 BIOS 화면으로 돌아갈 수 있습니다. **BIN 이름만 바꾸는 것으로 해결되지 않습니다. 이번 ZIP의 CUE를 사용하십시오.**

최종 폴더에는 다음 두 파일이 나란히 있어야 합니다.

```text
한국어판/
  Der Langrisser FX Korean.bin
  Der Langrisser FX Korean.cue
```

RetroArch에서는 BIN이 아니라 위 **CUE를 콘텐츠로 불러옵니다**. CHD가 필요하면 먼저 이 BIN/CUE로 정상 실행을 확인한 뒤, 이번 CUE를 입력으로 변환하십시오. 원본 CHD나 이전 한글판 CHD에 패치를 적용하지 마십시오.

### 적용 중 오류가 나는 경우

- 패치 파일이 보이지 않으면 ZIP을 먼저 풀었는지 확인하십시오. 배포 파일은 이미 `.xdelta`이므로 확장자를 바꿀 필요가 없습니다.
- `checksum mismatch` 등이 나오면 원본 BIN의 크기와 아래 SHA-256을 확인하십시오. 검사 기능을 끄거나 이미 패치한 BIN에 다시 적용하지 마십시오.
- 파일명이 자동으로 달라졌다면 최종 BIN 이름을 `Der Langrisser FX Korean.bin`으로 맞추십시오. CUE와 BIN은 같은 폴더에 있어야 합니다.

### Python 적용기(선택 사항)

원본과 결과의 SHA-256을 자동 검사하려는 분을 위한 보조 적용기입니다. 위 xdelta 방법으로 적용했다면 실행할 필요가 없습니다.

Python 3.9 이상과 `xdelta3`를 준비하고, 패치 압축을 푼 폴더에서 다음을 실행합니다. `원본폴더`는 실제 원본 BIN/CUE가 있는 경로로 바꾸고, `한국어판`은 아직 존재하지 않는 출력 폴더로 지정하십시오.

```sh
python apply_derl_pcfx_text_patch.py --source-bin "원본폴더/Der Langrisser FX.bin" --source-cue "원본폴더/Der Langrisser FX.cue" --output-dir "한국어판"
```

macOS·Linux에서 `python` 명령이 없으면 `python3`를 사용하십시오. xdelta3가 PATH에 없다면 `--xdelta3 "xdelta3 실행 파일 경로"`를 덧붙입니다.

## 패치 적용 결과

패처가 만드는 BIN과 ZIP에 동봉된 CUE를 같은 폴더에 준비합니다. 선택 사항인 Python 적용기는 두 파일을 함께 출력합니다.

- `Der Langrisser FX Korean.bin`
- `Der Langrisser FX Korean.cue`

결과 BIN:

- 크기: 778,808,352바이트
- SHA-256: `383741adcb59636728c649971db799041c32074c872a0ec50b15cf26a936bbd3`

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

글꼴과 제3자 구성요소의 출처 및 라이선스는 `CREDITS.md`, `THIRD_PARTY_NOTICES.md`, `OFL-1.1.txt`를 확인해 주십시오.
