# development guideline

## 1. develpment rule
* コードは、可読性を重要視し、誰が見ても理解できるコードを意識すること。  
（担当範囲が、入り乱れる／複数人による開発のため）
* コメントは極力残すこと。  
（必要最低限のドキュメントしか残さないので、極力コメントでフォローする）
* ミスを恐れない
* 単体テストは必ず実行する、自動化を必ず利用する（PHPUnit etc‥）

## 2. issue rule
* 設計／実装タスクは、必ず`github issue`を起こしてから着手すること。
* タスクには、`ToDo`, `goal`を明確にして記載すること。
* 着手中のタスクは、`In Progress`にし、担当者を明記すること。
* タスク担当者は、レビューが終わり問題がない場合は、`Done`に変更すること。
* レビュー時の指摘は、`pull-request`によるコメントで記載すること。

## 3. git rule
* 各リポジトリにて、以下のブランチ運用とする。
  * master・・・本番環境
  * develop・・・開発環境
  * feature/`<issue number>`・・・作業ブランチ
* `git commit`は小まめに実施し、できれば作業の最小単位で実施すること。
* コミットメッセージは、以下のフォーマットで記載する。  
   ```
   <issue number>: commit message.
   
   ex.
   #1: add login view.
   ```
* ローカル環境とリモート環境で差異がある場合は、`git pull`ではなく、`git rebase`で最新環境に合わせること。  
（ここがよくわからない人は、遠慮なく聞いてください。）
* `pull-request`の承認は、特定の人に依頼するのではなく、開発メンバーのうち２人がOKとして、`merge`を行う。
* `merge`を実施するのは、`pull-request`の依頼者とする。
* `pull-request`の依頼者は、`pull-request`を発行した場合、`@here`でslack全員に通知を送る
* `pull-request`を受けた側は、基本全員（最低２人）が承認できる状態で`pull-request`の依頼者が`merge`をする。


