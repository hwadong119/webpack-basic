## npm 설치

```terminal
npm init -y
```

<br><br>

## webpack 설치

```terminal
npm i -D webpack webpack-cli
```

```json
"devDependencies": {
    "webpack": "^5.88.2",
    "webpack-cli": "^5.1.4"
  }
```

빌드 스크립트 작성

```json
 "scripts": {
    "build": "webpack --mode production",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

<br><br>

## Build
```terminal
npm run build
```

import 기능 작성 후 build 하면 main.js에 업데이트

<br><br>

## Webpack Loader

- 로더(Loader)는 웹팩이 웹 애플리케이션을 해석할 때까지 자바스크립트 파일이 아닌 웹 자원(HTML, CSS, Images, 폰트 등)을 변화할 수 있도록 도와주는 속성

- 설치
  ```terminal
  npm i -D css-loader style-loader sass sass-loader
  ```

- style-loader: DOM에 스타일로 모듈 내보내기를 추가

- css-loader: 리졸브된 가져오기로 CSS 파일을 로드하고 CSS 코드를 반환

- less-loader: LESS 파일을 로드하고 컴파일

- sass-loader: SASS/SCSS 파일을 로드하고 컴파일

- postcss-loader: PostCss를 사용해 CSS/SSS 파일을 로드하고 변환

- stylus-loader: Stylus 파일을 로드하고 컴파일

<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
