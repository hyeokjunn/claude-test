# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

권혁준의 개인 포트폴리오 웹사이트입니다. 단일 HTML 파일로 구성되어 있으며, 모든 HTML, CSS, JavaScript가 `index.html`에 통합되어 있습니다.

## 로컬에서 실행하기

```bash
# Python 3를 사용한 로컬 서버 실행
python -m http.server 8000

# Node.js http-server를 사용한 실행 (설치 필요)
npx http-server
```

브라우저에서 `http://localhost:8000`으로 접속하거나, `index.html` 파일을 브라우저에서 직접 열어 실행할 수 있습니다.

## 코드 구조

`index.html`은 세 가지 섹션으로 구성됩니다:

- **HTML**:
  - Header 섹션: 프로필 이미지, 이름, 직업
  - Cards 섹션: 기술 스택, 학력, 소개 카드
  - Footer: 저작권 정보

- **CSS**: `<style>` 태그 내부에 모든 스타일 정의
  - Apple 디자인 스타일을 따르는 깔끔하고 미니멀한 디자인
  - 카드 기반 레이아웃
  - 부드러운 애니메이션과 호버 효과
  - 완전한 반응형 디자인 (모바일, 태블릿, 데스크톱)

- **JavaScript**: `<script>` 태그 내부에 로직 구현
  - `profileData` 객체: 프로필 데이터 관리
  - 페이지 로드 시 프로필 이미지 첫 글자 자동 설정
  - 스킬 태그 클릭 이벤트

## 프로필 정보 수정

프로필 정보는 `mycarrer.md` 파일에서 관리됩니다:

```
이름: 권혁준
주요 커리어: c언어,c++언어
출신학교: Uc 버클리
```

프로필 정보를 수정하려면:
1. `mycarrer.md` 파일의 내용을 수정
2. `index.html`의 해당 섹션을 수동으로 업데이트
   - 이름: HTML의 `.name` 클래스 요소와 JavaScript의 `profileData.name`
   - 기술 스택: `.skills-list` 내부의 스킬 태그와 `profileData.skills`
   - 학력: `.school-name` 요소와 `profileData.school`

## 디자인 특징

- **Apple 스타일**: 깔끔하고 미니멀한 디자인
- **색상 팔레트**:
  - 배경: 밝은 그레이 그라디언트 (#f5f7fa ~ #e8eef5)
  - 카드: 흰색 (#ffffff)
  - 텍스트: 다크 그레이 (#1d1d1f)
  - 보조 텍스트: 밝은 그레이 (#86868b)
  - 액센트: 보라-블루 그라디언트 (#667eea ~ #764ba2)
- **반응형 브레이크포인트**: 768px, 600px
