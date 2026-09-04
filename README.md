# 데어 랑그릿사 PC-FX 한국어 패치 v0.8.0

《데어 랑그릿사》 PC-FX판 비공식 한국어 패치 **v0.8.0 베타판**입니다. 대사·메뉴·정보창, 동영상 자막과 재생 복귀 수정, 전리품 메시지 수정, 후일담 출력 수정과 134개 문맥 교정까지 포함합니다. 원본에 이 패치 하나만 적용하며 과거 패치를 먼저 적용하지 않습니다.

**빛의 후예 시나리오는 제작자가 엔딩까지 직접 플레이하며 검수했습니다.** 다른 분기와 모든 후일담 조합의 검수까지 완료된 것은 아니므로 GitHub에서는 Pre-release로 제공합니다. 수정되지 않은 타이틀·로고·배경·이벤트 그림 속 문자는 전수 한글화 완료 범위가 아닙니다.

공개 버전은 `주.부.수정` 형식으로 표기하며 내부 개발 번호와 별도로 관리합니다.

## 다운로드

- [v0.8.0 베타 릴리스](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/releases/tag/v0.8.0)
- [패치 ZIP 다운로드](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/releases/download/v0.8.0/Der-Langrisser-PCFX-Korean-Patch-v0.8.0.zip)

v0.1.0과 패치 데이터·적용 결과는 동일합니다. 이미 적용하셨다면 다시 적용할 필요가 없습니다.

GitHub의 `Source code (zip)`이 아니라 위 패치 ZIP을 받으십시오. 패치·적용기·CUE·설명·고지·검증용 해시 목록이 함께 들어 있습니다. ROM과 BIOS는 제공하지 않습니다.

ZIP SHA-256:

```text
ba9ee5de8a86ac7778aac4131c108a6b1f289bb6ec828ab4c426f3e589504151
```

## 확인한 범위

- 제작자가 빛의 후예 시나리오를 엔딩까지 직접 플레이하며 검수했습니다.
- macOS에서 원본에 차분을 적용한 결과가 아래 목표 BIN/CUE 해시와 정확히 일치합니다.
- 동봉 적용기는 잘못된 원본 크기·BIN/CUE 해시·변조된 패치를 거부하고 기존 출력 폴더를 보호합니다.
- 이번 ZIP의 Windows·Linux 적용은 아직 확인하지 않았습니다. 아래 해당 OS 명령은 사용 안내이며 실행 검증 완료를 뜻하지 않습니다.

## 필요한 파일

사용자가 직접 보유한 아래 PC-FX 원본 두 파일이 필요합니다. 파일 내용이 정확히 일치하지 않으면 적용기는 결과 파일을 만들지 않습니다.

| 파일 | 크기 | SHA-256 |
|---|---:|---|
| `Der Langrisser FX.bin` | 775,880,112바이트 | `a1a2a501400bc5d9b3a06ba4600e4e7dee686974c089916c2b8f9ff7abb7cb73` |
| `Der Langrisser FX.cue` | 원본 파일 | `63679a3e577e4a940db89efd1db7df9159e95f88deab2a47848943ab123e67ef` |

Python 3.9 이상과 `xdelta3` 명령이 필요합니다. 이 패키지에는 실행 파일을 동봉하지 않습니다. 생성·로컬 적용 검증 대상은 macOS의 `xdelta3 3.1.0`이며, 이번 패키지의 실제 Windows·Linux 적용은 미검증입니다. 과거 패키지의 검증을 이번 버전의 결과로 간주하지 않습니다. 다른 호환 버전도 아래 목표 해시와 정확히 일치해야 성공합니다. xdelta는 [공식 프로젝트](https://github.com/jmacd/xdelta)에서 별도로 준비하십시오.

## 적용 방법

ZIP을 풀고 `apply_derl_pcfx_text_patch.py`가 있는 폴더에서 실행합니다. 원본 BIN/CUE에는 실제 보관 경로를 지정하십시오. 아래 예시는 두 원본 파일이 현재 폴더에도 있는 경우입니다. 출력 폴더는 적용 전에 존재하면 안 됩니다. 임시 출력용으로 약 1GB의 여유 공간이 필요합니다.

macOS·Linux:

```bash
python3 apply_derl_pcfx_text_patch.py \
  --source-bin "Der Langrisser FX.bin" \
  --source-cue "Der Langrisser FX.cue" \
  --output-dir "Der Langrisser FX Korean Test"
```

Windows PowerShell:

```powershell
py .\apply_derl_pcfx_text_patch.py `
  --source-bin ".\Der Langrisser FX.bin" `
  --source-cue ".\Der Langrisser FX.cue" `
  --output-dir ".\Der Langrisser FX Korean Test"
```

`xdelta3`가 기본 실행 경로에 없다면 끝에 `--xdelta3`와 실행 파일 경로를 추가합니다.

적용기는 다음 순서로 안전하게 처리합니다.

1. 원본 BIN 크기와 BIN/CUE SHA-256을 확인합니다.
2. VCDIFF와 동봉 CUE의 SHA-256을 확인합니다.
3. 새 임시 폴더에서만 결과를 만듭니다.
4. 결과 BIN/CUE의 크기와 SHA-256이 목표값과 정확히 일치할 때만 지정 출력 폴더로 확정합니다.
5. 기존 출력 폴더는 덮어쓰거나 삭제하지 않습니다.

성공한 결과는 다음과 같습니다.

| 파일 | 크기 | SHA-256 |
|---|---:|---|
| `Der Langrisser FX Korean Test.bin` | 778,669,584바이트 | `e3a31e66bbd6ca02a0f3aedc4008c2917f94b9d76e3674daba708735a4c3ef99` |
| `Der Langrisser FX Korean Test.cue` | 210바이트 | `81487b39a3d7db0853d737683bb23592eaeeebdb951204c6d0056bed45e2a915` |

에뮬레이터에서는 생성된 **CUE**를 여십시오. 원본 CUE를 결과 BIN에 재사용하지 마십시오. 기존 메모리카드 세이브는 별도로 백업하고, 세이브스테이트의 버전 간 호환성은 보장하지 않습니다.

## 추가 검수·오류 제보

빛의 후예 엔딩까지의 직접 검수는 완료됐습니다. 다른 분기나 아래 화면에서 문제를 발견하시면 알려 주십시오.

- 기본 주인공 이름이 `엘윈`으로 표시되는지
- 루시리스의 클래스 작성 질문과 선택지가 모두 한글인지
- 클래스·유닛·인명·병종·메뉴에 깨진 글자나 일본어 잔존이 없는지
- 스테이지 2 지휘관 배치에서 사각 커서와 깃발의 좌표가 일치하고 실제 배치가 가능한지
- 지휘관 목록에서 이름이 겹치지 않는지
- 대사의 줄바꿈·띄어쓰기·구두점·가독성과 진행에 문제가 없는지
- 동영상의 색상·움직임·자막 타이밍·건너뛰기·종료 뒤 게임 화면 복귀가 정상인지
- `소환`, `지휘범위`, `보정`과 전리품 획득·폐기·자동 장비 안내가 상황에 맞는지
- 모든 캐릭터의 후일담에서 조사·주체·문장 연결·페이지 전환이 자연스러운지

문제가 있으면 [Issues](https://github.com/lf-idonotknow/Der-Langrisser-PCFX-Korean-Patch/issues)에 패치 버전, 에뮬레이터, 발생 지점, 직전 조작과 화면을 기록해 주십시오. ROM·BIOS·세이브·계정정보·개인 경로는 첨부하지 마십시오.

## 크레딧과 변경 이력

- 작업 역할과 참고자료 출처: [CREDITS.md](CREDITS.md)
- 공개 버전별 변경 이력: [CHANGELOG.md](CHANGELOG.md)

## 배포 주의

- 이 패키지에는 원본 또는 패치된 전체 디스크 이미지가 들어 있지 않습니다.
- 원본 게임과 관련 상표·저작물의 권리는 각 권리자에게 있습니다.
- 한글 글꼴 고지는 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)와 [OFL-1.1.txt](OFL-1.1.txt)에서 확인할 수 있습니다.
