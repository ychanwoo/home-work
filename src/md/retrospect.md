# 멋쟁이사자 프론트엔드 1,2주차 회고

멋쟁이사자 프론트엔드 13기가 시작된 지 벌써 2주가 지났다.  
매일 아침 9시부터 저녁 6시까지 열정적으로 수업을 들으며 많은 것을 배웠다.

지난 2주 동안 Git과 Figma, 그리고 HTML 태그의 기초를 익혔다.  
처음 접하는 개념들도 많았지만, 하나하나 배워가는 과정이 흥미로웠다.  
특히 강사님께서 세심하게 설명해 주시고, 질문 하나도 놓치지 않고 답변해 주셔서 큰 도움이 되었다.

첫 주에는 9시 수업이 적응되지 않아 빈속에 커피를 마시며 하루를 시작하곤 했다.  
하지만 이제는 점점 익숙해지면서 새로운 생활 패턴으로 자리 잡은 것 같다.  
주말에는 조금 늦잠을 자는 소소한 행복을 누리며, 배운 내용을 정리하고 복습하는 시간을 가졌다.

앞으로 어떤 도전과 배움이 기다리고 있을지 모르지만, 주어진 모든 순간을 즐기며 최선을 다할 것이다. 파이팅!!!

---

# 1~2주차 회고 요약

## 1일차 회고

### 1. 필수 도구 설치

- **VS Code**
- **Git & GitBash**
- **NVM & Node.js** (자바스크립트 런타임 환경)
- **Oh My Zsh** (사양이 좋지 않다면 비추천)

### 2. Git 명령어

```bash
# 사용자 정보 설정
$ git config --global user.name "youngchan"

# Git Bash에서 Node.js 설치
$ nvm install lts
$ nvm use 22.13.1
```

---

## 2일차 회고

## CLI, Linux, Git 기본 개념 요약

### 1. CLI (Command Line Interface)

- **CLI**: 텍스트 명령어로 컴퓨터를 제어하는 인터페이스 (ex. `mkdir`, `cd`, `ls`, `rm`)
- **GUI (Graphic User Interface)**: 아이콘과 버튼을 이용한 조작 방식

### 2. Linux 기본 개념

- **리눅스**: UNIX 계열의 오픈소스 운영체제, 명령어 기반 작업
- **파일 시스템**: `/` (루트 디렉토리), `/home`, `/etc`, `/var` 등 주요 디렉토리
- **사용자 및 권한**: 사용자 계정, 파일 접근 권한 (읽기, 쓰기, 실행)

### 3. Git 기본 개념

- **Git**: 버전 관리 시스템, 파일 및 코드 변경사항 기록
- **Repository**: 프로젝트 파일과 그 이력을 저장하는 공간
- **Branch**: 독립적으로 작업할 수 있는 분기
- **Commit**: 변경 사항을 기록
- **Clone**: 원격 저장소의 복제
- **Push/Pull**: 원격 저장소와 로컬 저장소 간 데이터 송수신
- **Merge**: 여러 브랜치를 하나로 합치는 작업

---

## 3일차 회고

## Git checkout, switch, branch, merge 요약

### Git checkout

- **브랜치 변경**: `git checkout <branch_name>` 다른 브랜치로 이동
- **파일 복원**: `git checkout -- <filename>` 최신 커밋 상태로 파일 복구
- **커밋 간 이동**: `git checkout <commit-hash>` 특정 커밋으로 이동하여 작업

### Git switch

- **브랜치 전환**: `git switch <branch_name>`
- **새 브랜치 생성 후 전환**: `git switch -c <branch_name>`

### Git branch

- **브랜치 관리**: `git branch`, `git branch -a` (모든 로컬/원격 브랜치 조회)
- **새 브랜치 생성**: `git branch <branch_name>`
- **브랜치 삭제**: `git branch -d <branch_name>` (병합된 브랜치 삭제), `git branch -D <branch_name>` (강제로 삭제)
- **브랜치 비유**:
  - `main`: 본 공연
  - 새 브랜치: 리허설 무대
  - `git merge`: 리허설을 본 공연에 반영

### Git merge

- **병합 종류**:
  - **Fast Forward Merge**: 직선적인 병합
  - **Rebase Merge**: 기존 브랜치 내용 다시 확정 후 병합
  - **3-way Merge**: 공통 조상 기준 병합, 충돌 발생 시 해결 필요

### Git reset

- **`git reset` 종류**:
  - **soft**: HEAD만 이전 커밋으로 이동, staged 상태 유지
  - **mixed**: HEAD 이동 + 변경 사항 unstaged
  - **hard**: HEAD 이동 + 변경 사항 삭제 (복구 불가)
- **안전하게 되돌리기**: `soft` → `mixed` → `hard` 순으로 고려

### Git push, pull

- **`git push`**: 로컬 저장소 변경 사항을 원격 저장소로 전송
  - `git push origin <branch_name>`
- **`git pull`**: 원격 저장소의 변경 사항을 로컬로 가져와 병합
  - `git pull (origin main)` → `git pull`은 `git fetch` + `git merge` 결합

---

## 4일차 회고

### Figma 활용법 요약

#### 1. **UI 설계의 중요성**

- UI 설계는 사용자 경험을 향상시키며 개발자와 협업에 필수적임.
- **디자인 시스템**을 활용해 일관된 UI를 제공하고, **컴포넌트** 기반으로 효율적인 관리가 가능함.

#### 2. **Component & Instance**

- **Component**: 원본 컴포넌트, 모든 인스턴스에 반영됨
- **Instance**: 원본의 복사본, 일부 속성만 변경 가능

#### 3. **Component Variants**

- 하나의 컴포넌트 내에서 다양한 상태(예: 버튼의 기본, 호버, 클릭 상태)를 설정하여 효율적으로 관리할 수 있음.

#### 4. **Auto Layout**

- 요소들 간의 간격과 정렬을 자동으로 관리하며 반응형 디자인을 쉽게 적용할 수 있음.

#### 5. **단축키**

- `ctrl + p`: 검색 기능
- `shift + A`: Auto Layout 설정
- `ctrl + shift + click`: 다중 선택

---

## 5일차 회고

### 웹 개발 개요

#### 1. **웹의 역사**

- **웹의 아버지**: Tim Berners-Lee
- **웹 서비스의 목적**: 가까운 연결을 통해 멀리 있어도 가깝게 느껴짐
- **웹의 구성**:
  - **Front-End**: 사용자가 보는 웹 브라우저, 프레젠테이션 레이어
  - **Back-End**: 서버, 데이터베이스, 애플리케이션 레이어

### 2. **웹의 핵심 기술**

#### **HTML, CSS, JavaScript**

- **HTML**: 콘텐츠 구조화
- **CSS**: 스타일링
- **JavaScript**: 상호작용과 동작 구현

#### **Back-End 기술**

- **Node.js**: JavaScript로 서버 측 개발 가능
- **Express**: Node.js를 위한 빠르고 간단한 웹 애플리케이션 프레임워크
- **MySQL**: 관계형 데이터베이스 관리 시스템

### 3. **웹 접근성**

- **웹 접근성**: 장애가 있는 사람들도 웹을 사용할 수 있도록 보장하는 원칙
  - **Wcag 2.2**: 웹 콘텐츠 접근성 지침
    - 4가지 원칙: 인지 가능(P), 운용 가능(O), 이해 가능(U), 견고한(R)

### 4. **Node.js와 NPM**

#### **Node.js**

- **Node.js**: 서버 사이드에서 JavaScript 실행
- **특징**: 비동기식, 이벤트 기반, 빠르고 확장 가능
- **설치 방법**: `nvm`으로 Node.js 버전 관리

#### **NPM (Node Package Manager)**

- **패키지 설치**: 로컬 및 글로벌로 패키지 설치 가능
  - **로컬 설치**: `npm install <패키지명>`
  - **글로벌 설치**: `npm install -g <패키지명>`
- **사용 예시**: `add-gitignore` 패키지로 `.gitignore` 파일 생성

### 5. **웹 표준과 웹 접근성**

- **웹 표준 준수**: HTML, CSS, JavaScript 표준을 준수하여 웹 페이지 호환성 유지
- **웹 접근성 보장**: 장애가 있는 사용자가 웹을 불편 없이 사용할 수 있도록 지원
  - 예: 색 대비, 텍스트 대체 제공, 스크린 리더 지원 등

### 6. **기타 유용한 웹 개발 도구**

- **Git**: 버전 관리 시스템
- **GitHub**: 코드 저장소 및 협업 플랫폼
- **Visual Studio Code**: 코드 작성 및 디버깅을 위한 IDE

---

## 6일차 회고

### NPM

### `.gitignore`, `.prettierignore`와 무작위 파일 비교

- **`.prettierignore ./src --write`**: `home.html` 제외, 나머지 파일만 수정.
- **`.prettierignore ./src --check --ignore-path=.prettierignore`**: `.prettierignore`에 있는 파일 제외하고 나머지 수정.
- **`--ignore-path=.prettierignore / .gitignore`**: 해당 파일들 제외 후 나머지 파일 포맷팅됨.

> **npm 패키지 설치 시**: `npm install` 명령어 실행 후, `package.json`이 자동 생성됨.

- `npm init -y` 명령어와 동일한 효과.
- 패키지 추가 및 프로젝트 관리 가능.

### 패키지 설치 응용

- `--save-dev` 대신 `-D`로 사용 가능.
- 패키지명을 이어서 작성하면 동시에 설치.

### 패키지 설치 후 제거 방법

- 패키지 제거 시 `npm uninstall`로 제거.
- `rm -rf node_modules package-lock.json` 명령어로 npm 환경 초기화 가능.
- 순서:
  1. 먼저 패키지 삭제.
  2. `node_modules` 및 `package-lock.json` 삭제.

### 유용한 명령어 및 팁

- **`cp -r ssam-html-css learn-html-css`**: `-r` 옵션은 재귀적 복사.
- **`git push -u origin main`**: `-u`는 `--set-upstream` 단축어.
- **`git checkout -- index.html`**: `index.html` 파일 수정 전 상태로 되돌리기.
- **`git add .`**: 현재 디렉토리 및 하위 디렉토리의 모든 변경된 파일을 스테이지에 추가.

### HTML

- **HTML (HyperText Markup Language)**: 웹에 표시되는 문서의 구조를 정의하는 표준 마크업 언어.
- **DOM 트리 구조**: `<head>`와 `<body>`를 자식으로 가지며, `<head>`는 `meta`, `title` 등의 자식을 가짐.
- **Empty Element**: content와 closing tag가 없는 태그 (예: `<img />`, `<br />`).

#### 기본 구조

```html
<!DOCTYPE html>
<html lang="en-US">
  <head> </head>
  <body></body>
</html>
```

---

## 7일차 회고

### EXTENSIONS에서 Material Theme Icons 설치

- `Material Theme Icons`를 설치하면 파일 아이콘을 변경할 수 있음

### 테마 변경

- `Eva`, `palenight Theme` 등을 설치하면 코드 테마를 변경할 수 있습니다. -> 현재 EVa 테마 사용중!

### 웹페이지에서 렌더링이 이루어지는 영역: `body` 태그의 역할

- HTML 문서에서 렌더링(rendering)이 이루어지는 주요 영역은 `<body>` 태그
  즉, 사용자가 브라우저를 통해 직접 확인할 수 있는 콘텐츠는 모두 `<body>` 내부에 포함되며, 이는 웹사이트의 시각적 요소와 상호작용을 담당하는 핵심 구조라고 할 수 있음.

### 절대경로와 상대경로

#### **절대 경로**

- 최상위 디렉토리부터 해당 파일까지 경유한 모든 경로를 전부 기입하는 방식
- `/src/html/index.html` or `https:/www.naver.com`
- 로컬에서의 절대경로 → `file:///c:/user/src/index.html`
- `https://localhost:3000/src/html/index.html` → 내 컴퓨터에만 보이는 주소
- 절대 경로를 주로 사용함 (프로젝트)
- 배포 안됨

#### **상대 경로**

- 현재 파일이 존재하는 디렉토리를 기준으로 해당 파일까지의 위치를 작성한 경로
- `./src/html/index.html` & `../src/html/index.html`
- github에 배포시 상대경로 사용

**개발자와 HTML을 공유하는 경우 → "무조건 절대 경로 사용" / 이외에는 "상대경로"**

### 이미지와 피규어

- HTML 문서에는 텍스트 이외에 <img> 요소와 도표, 차트, 표, 이미지 등 캡션과 함께 묶어주는 <figure> 요소가 있음

#### 이미지

`<img src = "images/eve.png" alt = "Eve">`

- `src` 는 source의 약자로 image의 경로를 확장자와 함께 작성함
- `alt` (alternative text) 속성은 이미지가 로드되지 않을 때 표시되는 대체 텍스트임
- 대체 텍스트는 이미지를 그대로 전달하기 위한 텍스트 입력
- `.webp`(Web Picture Format) 확장자 →구글(Google)에서 개발한 차세대 이미지 포맷
- 이미지 최적화를 위해선 `.jpeg` 보다 `.wepb` 확장자 사용 → 용량 훨씬 적음
- `.svg` 이미지 파일 코드에서 대체 텍스트 (`alt`)를 입력하는 코드 `aria-label=” ”`
- `<title> 이미지 대체 텍스트 <title />` 도 대체 텍스트 가능함
