# ヒトコール AI接続パッケージ

ChatGPTデスクトップ/Codex用 `.codex-plugin/plugin.json`、Claude Code用 `.claude-plugin/plugin.json`、Antigravity CLI用 `plugin.json` / `mcp_config.json`、対応契約のGemini CLI用 `gemini-extension.json`、共通のMCP設定と操作スキルを収録しています。秘密キーを含みません。接続はOAuthで本人が許可します。

## 公開リポジトリから追加

Claude Code:

```bash
claude plugin marketplace add JapanMarketing-Dev/hitocall-plugin
claude plugin install hitocall@hitocall
```

Gemini CLI（Code Assist Standard / Enterprise、または有料APIキー利用者）:

```bash
gemini extensions install https://github.com/JapanMarketing-Dev/hitocall-plugin
```

個人向けのGemini CLI（無料・Google AI Pro / Ultra）は2026年6月18日からAntigravityへ移行しました。Antigravity CLIは下記のZIPから追加できます。旧CLIを個人アカウントで起動する手順は使わないでください。
[Googleの移行案内](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/)

この配布元はJapanMarketingが運営する公開カタログです。各AI事業者の公式ディレクトリ掲載とは別です。

## ダウンロード後の導入

ZIPを展開すると `hitocall` フォルダができます。

Claude Code（セッションで読み込み）:

```bash
claude --plugin-dir ./hitocall
```

Antigravity CLI（Geminiを使う現在の個人向けCLI）:

```bash
agy plugin install ./hitocall
```

Antigravityを開き、`/mcp` からヒトコールの接続状態を確認して認証します。

Gemini CLI（対応契約の利用者）:

```bash
gemini extensions install ./hitocall
```

Gemini CLIの起動後に `/mcp auth hitocall`、Claude Codeでは `/mcp` から認証してください。最初に「ヒトコールの初期設定を進めて」と依頼します。

ChatGPT/Codex: プラグインのストア掲載は未実施です。ローカルプラグインを扱える開発環境で検証するためのmanifestを同梱しています。一般利用者は https://hitocall.com/docs のMCP接続手順を使ってください。

Microsoft 365 Copilot: 別配布の `hitocall-m365.zip` を使用します。
Gemini Web: Gemini SparkのカスタムConnected AppsでMCP URLを追加します。地域・アカウントの提供条件はGoogle公式ヘルプを確認してください。

OAuth接続先は本番配備済みです。各社の公式ストアには未掲載です。接続手順と提供状況は https://hitocall.com/docs を確認してください。
