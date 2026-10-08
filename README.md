# Ilshin Application Releases

(주)일신이디아이 주요 애플리케이션의 공식 설치 및 업데이트 배포 저장소입니다.

모든 최신 배포본은 [Releases 페이지](../../releases)에서 제품별 태그를 통해 다운로드하실 수 있습니다.

---

## 1. 릴리스 명명 규칙 (Naming Convention)

각 제품은 고유 접두사(Prefix)와 버전 규칙을 기준으로 구분 배포됩니다.

| 제품명 | 태그 형식 | 설치 파일 (Full Setup) | 패치 파일 (Patch) |
| :--- | :--- | :--- | :--- |
| **PAMS.Web** | `pams-web-v*.*.*` | `PAMS.Web.UI-setup-*.exe` | `PAMS.Web.UI-patch-*.exe` |

> **다운로드 가이드**
> * **Setup 파일**: 신규 PC에 처음 프로그램을 설치하거나 전체 재설치가 필요할 때 사용합니다.
> * **Patch 파일**: 기존 프로그램이 설치된 PC에서 빠른 버전 업데이트 시 사용합니다.

---

## 2. 제품별 설치 및 패치 가이드

### [PAMS.Web]

* **기본 설치 경로**: `C:\IlshinEDI\Bin\PAMS.Web`
* **실행 환경**: Windows (x86, .NET 8.0 런타임 내장)
* **신규 설치**:
  1. `PAMS.Web.UI-setup-*.exe`를 관리자 권한으로 실행하여 설치합니다.
  2. 설치 완료 후 설치 경로 내 `install-service.bat`를 **관리자 권한으로 실행**합니다. (윈도우 서비스 등록 및 통신 방화벽 자동 구성)
* **패치 업데이트**:
  1. `install-service.bat` 또는 서비스 관리자에서 `PAMS_Web_Service` 상태를 확인 후 패치 파일(`PAMS.Web.UI-patch-*.exe`)을 실행합니다
  2. 업데이트 완료 후 서비스를 재시작합니다.
* **서비스 관리 안내**:
  * `install-service.bat`: 윈도우 서비스 자동 등록, 자동 복구 설정, 필수 통신 방화벽 규칙 일괄 개방
  * `uninstall-service.bat`: 윈도우 서비스 제거 및 등록된 방화벽 규칙 원복

---

### [(추가 예정 제품)]

* **기본 설치 경로**: `C:\IlshinEDI\Bin\...`
* **설명**: 신규 제품 릴리스 시 해당 항목에 기본 정보와 실행 안내가 추가됩니다.
