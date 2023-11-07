## 프로젝트 설명

- 출석용 nft 지갑 만들기 프로젝트 수행




<br />

## 옵셔널 세팅

### `shift + command + x` 눌러서 `eslint extension` 설치 (optional)

### (Optional) caver 호환성 문제

```js
module.exports = {
    ...
    resolve: {
        fallback: {
            fs: false,
            net: false,
            stream: require.resolve('stream-browserify'),
            crypto: require.resolve('crypto-browserify'),
            http: require.resolve('stream-http'),
            https: require.resolve('https-browserify'),
            os: require.resolve('os-browserify/browser'),
            ...
        },
    },

    plugins: [
      new webpack.ProvidePlugin({
        Buffer: ['buffer', 'Buffer'],
      }),
      ...
    ],
}
```
