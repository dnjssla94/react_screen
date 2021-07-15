# 프로젝트 실행 및 설명

리엑트 라이브러리를 사용하여 방카 청약 화면의 일부를 구현하였습니다.



## 프로젝트 실행

1. 프로젝트를 로컬에 clone하고  터미널창으로 해당 경로로 들어가서 작업함.



​	2-1. nodejs 및 npm 설치 여부 확인

```npm 
node -v
npm -v
```

​	2-2. 설치 안되어있다면 nodejs, node 설치
참고: https://joyfulhome.tistory.com/180

​	2-3. 설치되어있다면 업데이트

```npm -update
npm -update
```



​	3-1 yarn 설치 여부 확인

```yarn -version
yarn --version
```

​	3-2 설치 안되어있다면 yarn 설치

```npm install --grobal yarn
npm install --grobal yarn
```

​	3-3 설치되어있다면 업그레이드

```yarn upgrade
// 이 명령은 모든 의존 패키지를 package.json 에 정의한 버전의 범위에서 업데이트하거나 삭제합니다
yarn upgrade
```



### 구조

프로젝트 주요 컴포턴트

- public: 적적인(static) 파일 관리 
- src: 동적인 파일 관리
  - compoents
    - comboBox.jsx
    - contentTable.jsx
    - radioButton.jsx
    - textBox.jsx
  - App.jsx: 메인 화면
  - index.js: 화면 렌더링
- package.json: 패키지 버전관리



### 세부 코드

0. React 컴포넌트 기본구성

1.  ../src/App.jsx
2. ../src/components/contentTable.jsx
3. ../src/components/radioButton.jsx
4. ../src/components/textBox.jsx
5. ../src/components/comboBox.jsx
