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

## 파일 이름에 Hash 값 주는 법

```js
output: {
    path: path.resolve(__dirname, 'dist'),
    filename: '[name][contenthash].js',
  },
```

- 이전 해시 파일을 자동으로 지워주려면
```js
output: {
    path: path.resolve(__dirname, 'dist'),
    filename: '[name][contenthash].js',
    clean: true
  },
```

<br><br>

## Babel Loader

- 구버전 브라우저에서도 최신 자바스크립트 코드로 이루어진 앱을 이용할 수 있게 ES5 이하의 코드로 프랜스파일링 하도록 하는 기능이 바벨

- 웹팩으로 파일을 번들링할 때도 바벨을 사용할 수 있게 해주는 것이 babel-loader

- 설치

  ```terminal
  npm install -D babel-loader @babel/core @babel/preset-env
  ```
- 사용법

  ```js
  {
    test: /\.js$/,
    exclude: /node_modules/,
    use: {
      loader: 'babel-loader',
      option: {
        presets: ['@babel/preset-env']
      }
    }
  }
  ```

<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
