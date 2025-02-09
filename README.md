# qiita

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

Citations:
[1] https://qiita.com/Qiita/items/32c79014509987541130
[2] https://qiita.com/ryocha12/items/e412306f9e8339d7cffe
[3] https://github.com/increments/qiita-cli/blob/main/README.md
[4] https://qiita.com/t_kyn/items/e6620762584921da9c6d
[5] https://zenn.dev/shogo_wada_pro/articles/35db506b92caae
[6] https://qiita.com/torifukukaiou/items/75854acfcb0460d08237
[7] https://zenn.dev/noraworld/articles/github-to-qiita
[8] https://qiita.com/ryokat3/items/d054b95f68810f70b136

---
Perplexity の Eliot より: pplx.ai/share