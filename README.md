# TypeScript & React & Webpack 最小構成
[React & Webpack · TypeScript](https://www.typescriptlang.org/docs/handbook/react-&-webpack.html)
- webpack-dev-server なし
- .editorconfig なし
- TSLint なし
- その他 Redux 等なし

## インストール
```
$ npm install
```

## ビルド
### 開発ビルド
```
$ npm run build
```
→ dist フォルダへ出力

### 開発ビルド(ファイル更新時自動ビルド)
```
$ npm run build:w
```
ただし、いずれにしろブラウザ側では F5 押す必要がある  
なので、もっと楽するなら webpack-dev-server 入れる(F5 すら不要)

### 製品ビルド
```
npm run build:p
```
externals 指定していないので react/react-dom も bundle.js に組み込まれる  
なので index.html 内の react/react-dom の script タグを削除してよい

## 実行
### WebStorm の場合
index.html のコンテキストメニューから open in browser > Default  
単に index.html をブラウザに D＆D しただけでは React DevTools を使用できないので注意



## 参考
[TypeScriptでReactを書く – webpackを使った開発環境の構築方法 | maesblog](https://mae.chab.in/archives/59782)


