# 프로젝트 실행 및 설명

리엑트 라이브러리를 사용하여 방카 청약 화면의 일부를 구현하였습니다.



## 프로젝트 실행

1-1프로젝트를 로컬에 clone하고  해당 경로에서 작업.



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



### 프로젝트 구조

#### 프로젝트 주요 컴포턴트

- public: 정적인(static) 파일 관리 
- src: 동적인 파일 관리
  - compoents
    - comboBox.jsx
    - contentTable.jsx
    - radioButton.jsx
    - textBox.jsx
  - App.jsx: 메인 화면
  - index.js: 화면 렌더링
- package.json: 패키지 버전관리



### 세부 내용

#### 0. React 컴포넌트 기본 구성

- 리엑트는 컴포넌트들의 집합입니다. 컴포넌트는 class와 function 두가지 방법으로 구성이 가능합니다. 

- function 방식(react hook)은 비교적 최근에 도입되어 불안정한 측면이 있어, 본 프로젝트에는 class 방식의 react 컴포넌트를 사용하였습니다. 

- 아래는 class 방식 react component의 기본 구조입니다.

  ```
  import './App.css';
  import React, { Component } from 'react';
  
  class App extends Component {
  	state = {
  	}
  	
  	메서드들...
  	
  	render() {
  		return(
  			<>
  			</>
  		) 
  	}
  }
  export default App;
  ```

  state 객체는 데이터를 관리합니다. 
  render 내부의 return 값은 html 영역입니다.

#### 1.  ../src/App.jsx

- React에서 data는 기본적으로 부모 컴포넌트에서 자식 컴포넌트로 이동합니다. SPA에서 전체 화면을 관리하는 가장 상위의 컴포넌트 입니다.
- 모든 data는 이 App 컴포넌트의 state에서 관리합니다. 
  - (setState()를 통해서 state값을 변경하면 react가 자동으로 render()를 호출하여 화면을 변환합니다.)
- 자식 컴포넌트로 데이터를 보내거나, 데이터를 가져와서 로직을 처리하는 함수들이 class 안에 정의되어있습니다.

#### 2. ../src/components/contentTable.jsx

- table(grid)을 그리는 함수입니다. 
- comboBox 컴포넌트를 자식으로 갖고있습니다.
- comboBox로 데이터를 보내기도 하며, comboBox의 데이터를 받아서 App으로 보내는 메서드도 정의되어있습니다.

#### 3. ../src/components/radioButton.jsx

- 부모 컴포넌트로 데이터를 전송하는 라디오 버튼이 구현되어있는데, 현재 프로젝트에서는 쓰이지 않습니다.

#### 4. ../src/components/textBox.jsx

- input text box를 그리는 함수입니다.
- 부모 컴포넌트로 text box에 입력한 값을 전송하는 메서드가 정의되어 있습니다.

#### 5. ../src/components/comboBox.jsx

- combo box를 그리는 컴포넌트 입니다.
- combo box에 보여지는 데이터는 동적으로 받아오게 되므로 모든 콤보박스에 재사용이 가능하도록 구현되어있습니다.
- 부모 컴포넌트로 선택된 값을  전송하는 메서드가 정의되어있습니다.

