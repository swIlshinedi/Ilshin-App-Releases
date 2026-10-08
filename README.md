## 배포 및 설치 안내

### 1. 배포 파일 구분
* **Full Setup (`PAMS.Web.UI-setup-*.exe`)**: 신규 설치 시 사용합니다. 프로그램 및 필수 구성 요소를 시스템에 전체 등록합니다.
* **Patch (`PAMS.Web.UI-patch-*.exe`)**: 기존 설치 버전을 업데이트할 때 사용합니다. 기존 설정 유지 상태로 실행 파일 및 리소스를 덮어씁니다.

> 최신 설치/패치 파일은 [Ilshin-App-Releases Releases](https://github.com/swIlshinedi/Ilshin-App-Releases/releases)에서 다운로드할 수 있습니다.

---

### 2. 기본 설치 정보
* **기본 설치 경로**: `C:\IlshinEDI\Bin\PAMS.Web`
* **실행 환경**: Windows x86 (.NET 8.0 런타임 자체 포함)
---

### 3. 설치 및 패치 적용 순서

#### 신규 설치
1. `PAMS.Web.UI-setup-*.exe`를 관리자 권한으로 실행하여 설치를 완료합니다.
2. 설치 폴더(`C:\IlshinEDI\Bin\PAMS.Web`)에서 `install-service.bat`를 마우스 우클릭 후 **관리자 권한으로 실행**합니다. (윈도우 서비스 자동 등록 및 방화벽 개방)

#### 패치 업데이트
1. `uninstall-service.bat`를 실행합니다.
2. `PAMS.Web.UI-patch-*.exe`를 실행하여 패치를 적용합니다. (기본 설치 경로로 자동 추출)
3. `install-service.bat`를 실행하여 서비스를 재기동합니다.

---

### 4. 서비스 관리 스크립트
설치 경로 내 배치 스크립트를 통해 서비스를 손쉽게 관리할 수 있습니다:
* `install-service.bat`: 윈도우 서비스 자동 생성, 장애 시 자동 재시작 정책 설정, 인바운드 방화벽 규칙 일괄 등록
* `uninstall-service.bat`: 실행 중인 서비스 중지/삭제 및 등록된 방화벽 규칙 원복
