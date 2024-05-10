## 概要
* スレッド内でチャットメッセージが届いた際に募集管理者にメール通知が届くようにする 

## 変更内容
* `offer_thread_messages_controller.rb`内`create`メソッドにてメッセージ送信後のメール送信メソッド呼び出しを追加
* `offer_mail_sender_job.rb`にスレッド内返信時メール通知用新規メソッドの追加
* スレッド内返信時メールファイル新規作成

## 関連チケット
[teams_INFRA-105](https://sporture1.backlog.jp/view/INFRA-105)

## 参考
## 公開設定を表示にした際の挙動

- スレッド内新規作成時通知メール
    

![image](https://github.com/DaisukeKikukawa/pr_draft/assets/58897760/23db1800-350b-413c-883a-7cca9fc1467d)



## 共有
[テスト項目](https://docs.google.com/spreadsheets/d/1fgmJKnTt9kvnECYnwOVC0WdSIVzS4KHLF8ynowW0Q4E/edit#gid=1570625385)

