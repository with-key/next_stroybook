# Next 14, Storybook 7, vanilla extract

1. 스토리북 초기 설치
```
npx storybook@latest init
```

2. vanilla extract 및 Next.js 설정 패키지 설치
```
npm install @vanilla-extract/css
```

```
npm install --save-dev @vanilla-extract/next-plugin
```

3. vanilla extract next.config.js 설정
```js
const {
  createVanillaExtractPlugin
} = require('@vanilla-extract/next-plugin');
const withVanillaExtract = createVanillaExtractPlugin();

/** @type {import('next').NextConfig} */
const nextConfig = {};

module.exports = withVanillaExtract(nextConfig);
```

4. vanilla extract .storybook/main.ts 설정 패키지 설치
```
npm install --save-dev @vanilla-extract/webpack-plugin mini-css-extract-plugin
```

5. vanilla extract, Storybook 설정 적용 CLI 실행
```
npx storybook@latest add @storybook/addon-styling-webpack
```

> 설정 마치고 스토리북 실행 오류 시, node_momodules 재설치