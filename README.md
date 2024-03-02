# dependa-gha-experiment

## これはなに

2024.03.01 時点で非推奨な Node16 に依存している action を使っていた場合、dependabot はどういう PR を作ってくれるのかという実験場。  

https://docs.github.com/ja/code-security/dependabot/dependabot-version-updates/about-dependabot-version-updates#github-actions によると、custom action や reusable workflows は更新対象にしない。  

> Dependabot will ignore actions or reusable workflows referenced locally (for example, ./.github/actions/foo.yml).

ローカルの custom action の中身までチェックしてくれないのは不便だが、本当にそうなのか試してみた。  

## 結果

公式ドキュメントの通り、`.github/workflows` 直下しか見ませんでした。悲C。  

- https://github.com/guricerin/dependa-gha-experiment/pull/1
