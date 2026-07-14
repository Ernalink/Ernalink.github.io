# Ernalink.github.io — ernalink 屋号サイト

GitHub Pages で配信する ernalink の対外ページ（トップ・事業者情報・製品紹介・プライバシーポリシー・サポート）。

- 公開URL：`https://ernalink.com/`（カスタムドメイン設定後）／`https://ernalink.github.io/`
- 実装：素の HTML + `assets/style.css` の1枚CSS。ビルド不要（push＝公開）。

## 構成

```
/                          … トップ（屋号サイト）
/about.html                … 事業者情報
/reception-desk/           … RD 紹介 ─ privacy.html / support.html
/simple-sipphone/          … SP 紹介 ─ privacy.html / support.html
/assets/style.css          … 共通CSS（クラスを増やす前にここを見る）
```

**ストア登録URL・アプリ内リンクは `https://ernalink.com/...` に統一する。**

| 用途 | URL |
|---|---|
| RD プライバシーポリシー | `https://ernalink.com/reception-desk/privacy.html` |
| RD サポート | `https://ernalink.com/reception-desk/support.html` |
| SP プライバシーポリシー | `https://ernalink.com/simple-sipphone/privacy.html` |
| SP サポート | `https://ernalink.com/simple-sipphone/support.html` |

## カスタムドメイン（ernalink.com）

**DNS を Cloudflare に設定してから、GitHub の Settings → Pages → Custom domain に `ernalink.com` を入力する**
（GitHub が `CNAME` ファイルを自動コミットする。手で先に置かないこと）。

> ⚠️ **順序が逆だと新サイトが見えなくなる。** `CNAME` があると GitHub Pages は
> `ernalink.github.io` → `ernalink.com` へリダイレクトするため、DNS 未設定の段階で置くと
> どちらのURLからも到達できなくなる。DNS 開通を確認してから設定すること。

## 旧リポジトリ `Ernalink/reception-desk-privacy-Policy` について

**まだ生きている。消さない。** 公開済みアプリ（TestFlight / Play）と両ストアのメタデータには
旧URL `https://ernalink.github.io/reception-desk-privacy-Policy/...` が登録されており、
旧リポジトリはそれを配信し続けている。本リポジトリは**別リポジトリとして新規作成**したため、
旧URLはリネームによる 404 を起こさずそのまま生きる。

**廃止条件**：両アプリの次回ストア提出で Support URL / プライバシーポリシーURL が
`ernalink.com` 系に更新され、旧URLがどこからも参照されなくなったら、旧リポジトリをアーカイブする。
それまでは**両サイトの内容が二重管理**になる点に注意（ポリシー本文を直すときは両方直すか、
旧リポジトリ側をリダイレクトHTMLに差し替える）。
