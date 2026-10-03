# Cherry Clock · 벚꽃 시계

기상청 23개 관측지점의 벚나무 첫 개화일을 탐색하는 브라우저 기반 연구 프로그램입니다.

**웹 프로그램:** https://mingming116.github.io/Cherry-Clock/

## 실행

- 웹에서는 위 주소로 접속합니다.
- 오프라인에서는 `index.html`을 내려받아 브라우저로 엽니다.
- 별도의 설치, 로그인, 서버 또는 자료 업로드가 필요하지 않습니다.
- 화면의 **HTML 저장**으로 코드·내장자료가 포함된 독립 실행 파일을, **결과 CSV 저장**으로 선택 조건의 지점별 결과를 받을 수 있습니다.

## 주요 기능

- **2027년 전망:** 과거 기상경로를 이용하는 연간 기후적 사전 전망
- **연구 재현:** 이전 자료로 학습한 매개변수를 사용하는 과거 시점 계산
- **논문 결과:** 최종 연구의 모형별 성능 및 기상정보 민감도
- 23개 관측지점 지도, 기온 변화, 계산 과정, CSV 내보내기

브라우저에서 직접 계산하는 모형은 parallel model (PA)과 thermal time model (TT)입니다. 다른 모형의 논문 성능은 저장된 연구 결과로 표시합니다. 수치예보를 실시간으로 수신하는 프로그램은 아니며, 과거 기상경로의 10–90분위수는 보정된 80% 예측구간이 아닙니다. 목표는 관측목의 첫 개화일입니다.

## 연구 자료

Prepared inputs, model checkpoints and case-level results for cherry flowering prediction at 23 Korean stations, version 1.0.0.

**Zenodo:** https://doi.org/10.5281/zenodo.23057582

연구자: Minwoo Kim, Yun-Ho Oh, Jaeyoung Jang, Jina Kim, Dong-Jun Lee, Hyeonah Lee.

본 연구는 농촌진흥청 과제 「농생명데이터 품질관리, 통합제공 및 대화형 서비스 AI 기술 개발」(PJ01778803)의 지원으로 수행되었습니다.

## 자료 출처와 라이선스

- 기상·계절관측과 지점 정보: 기상청. 가공자료에도 원자료의 출처표시 조건을 유지합니다. 구체적인 구성요소별 조건은 Zenodo 패키지의 `RIGHTS.md`와 `DATA_SOURCES.md`를 참고합니다.
- 해안선: Natural Earth, public domain.
- PA·TT 계산 코드는 Koen Hufkens 등의 [phenor](https://github.com/bluegreen-labs/phenor) 1.3.1에서 이식되었습니다. 기존 프로그램에 명시된 **AGPL-3.0**과 저작자 고지를 유지합니다. [LICENSE](LICENSE)에 라이선스 전문이 있습니다.
- 계산 코드, CSS, 내장자료, 이미지 및 라이선스는 모두 `index.html`에 들어 있습니다. 배포 파일 자체가 전체 브라우저 애플리케이션 소스입니다.

## GitHub Pages

이 저장소는 빌드가 필요 없는 정적 사이트입니다.

1. **Settings → Pages**를 엽니다.
2. **Source → Deploy from a branch**를 선택합니다.
3. **Branch → main**, 폴더 **/(root)**를 선택하고 저장합니다.
4. 이후 `main`의 `index.html` 변경 사항이 Pages에 반영됩니다.

`.nojekyll`은 정적 파일을 그대로 제공하도록 하는 설정 파일입니다. 전망 자료의 연간 갱신은 별도의 자료 검토·모형 적합·검증 후 수행해야 하며, 웹 배포만으로 내장자료가 자동 갱신되지는 않습니다.

## 배포 기준

- 기반 파일: `Cherry_Clock_Offline_20260930.html`
- GitHub 배포 준비: 2026-10-03
- 배포 시 수정: 미입력 상태였던 연구 자료 DOI 두 곳 반영
