# 公開手順

このサイトは、`main`ブランチへのPushをきっかけにGitHub ActionsからPleskへ自動公開します。

## 初回設定

GitHubリポジトリの **Settings → Secrets and variables → Actions** を開き、次のRepository secretsを登録します。

| Secret名 | 設定する値 |
| --- | --- |
| `FTP_SERVER` | FTPホスト名 |
| `FTP_USERNAME` | FTPアカウント名 |
| `FTP_PASSWORD` | FTPパスワード |

パスワードなどの実際の値は、リポジトリ内のファイルへ記載しないでください。

## 通常の更新

```bash
git add .
git commit -m "変更内容"
git push origin main
```

Push後はGitHubの **Actions → Deploy website** で公開結果を確認します。

## 手動で再公開する場合

GitHubの **Actions → Deploy website → Run workflow** から実行できます。
