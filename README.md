# qiita

<details>

<summary>Perplexity</summary>

Qiitaの記事をGitHubで管理するには、以下の手順を実行します：

1. GitHubでリポジトリを作成します[1][3]。

2. Qiitaの個人用アクセストークンを発行します。Qiitaの設定から「アプリケーション > 新しくトークンを発行する」を選択し、read_qiitaとwrite_qiitaのスコープにチェックを入れてトークンを生成します[1]。

3. 作成したGitHubリポジトリの設定から、Secrets and variablesのActionsセクションに移動し、「New repository secret」をクリックします。Nameに「QIITA_TOKEN」、Secretに発行したQiitaのアクセストークンを設定します[1][3]。

4. ローカル環境にQiita CLIをインストールします：

```bash
npm install @qiita/qiita-cli --save-dev
```

5. Qiita CLIをセットアップし、必要なファイルを生成します：

```bash
npx qiita init
```

6. 既存のQiita記事をローカルに取得します：

```bash
npx qiita pull
```

7. 生成されたファイルとQiitaから取得した記事をGitHubリポジトリにプッシュします[1][2]。

これらの手順を完了すると、GitHubリポジトリにプッシュした際に自動的にQiitaに記事が投稿・更新されるようになります[1][3]。記事の編集は.mdファイルを修正し、再度プッシュすることで行えます[1]。

この方法を使用することで、好みのエディタで記事を執筆し、Gitの機能を活用して編集履歴を管理できるようになります[7]。

</details>