# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

- 목적: SAP와 외부 서비스 연동 (README 기준)
- 현재 상태: 초기 커밋만 있고 README 외 소스·빌드 설정·테스트가 없다. 기술 스택, 연동 방식(RFC/BAPI, OData, IDoc 등), 디렉터리 구조는 아직 정해지지 않았다.

## 작업 시 유의사항

- 상위 워크스페이스 지침 `D:\00AI_Workspace\Claude\CLAUDE.md`가 함께 적용된다. 보안, 개인정보, 소스 외부 노출 금지, ABAP Include 분리, 파일 길이 제한이 여기에 정의되어 있고 hook으로 강제된다. 이 파일에서 같은 내용을 반복하지 않는다.
- 기술 스택과 연동 방식이 정해지지 않았으므로 임의로 정하지 말고 사용자에게 확인한다.

## 빌드·테스트 명령

아직 없음. 프로젝트 구성이 추가되면 빌드·린트·전체/단일 테스트 실행 명령을 이 섹션에 기록한다.

## 아키텍처

아직 없음. 코드가 추가되면 SAP 연동 계층, 외부 서비스 클라이언트, 설정·자격증명 주입 방식 등 여러 파일을 읽어야 파악되는 전체 구조를 이 섹션에 기록한다.

## 기획 진행 현황 (세션 시작 시 먼저 읽기)

- 대화·결정 기록: `docs/CONVERSATION_LOG.md` — 새 세션은 이 파일을 먼저 읽고 이어서 작업한다. 작업이 끝나면 같은 형식으로 항목을 추가한다.
- 현재 기획 버전: v0.5 (프로토타입), 기획서 v0.4
- 산출물 위치: `prototype/`(HTML 프로토타입 버전별), `backup/vX.Y/`(이전 버전 기획서·프로토타입 백업)
- 정해진 사항(2026-11-16 기준, 확정 아님 — 기획 단계): 연동 경로 Web(BFF) → BSG AWS EAI → SAP RFC, 로그인 fs.golfzon.com(Entra ID) SSO 단일, 메뉴는 SAP 모듈(FI/SD/MM/CO/PP/LE) → 하위 모듈 → 프로그램 구조, 권한은 AGR_USERS/AGR_TCODES 기준 노출 + SAP 측 재검사
- 위 내용은 기획안이며 기술 스택·연동 방식 확정 전에는 코드 작성 전 사용자 확인을 받는다.
