# pr_draft

## 概要
* 【球場一覧画面】表示・非表示設定をできるようにする
*  【日程・結果画面】のグラウンド登録する際、プルダウンメニューの非表示設定が影響しないよう確認する

## 変更内容
* グラウンド一覧で表示・非表示の管理をするための`is_displayed`カラムを新たにグラウンドテーブルに追加
* グランドの表示・非表示設定用の`_select_form.html.erb`を新たにパーシャルとして追加し、`_form.html.erb`で呼び出し
* `is_displayed`カラム用のバリーでションをグラウンドモデルに追加
* `is_displayed`カラムが`true`の値のみを取得する`scope`を新たにグラウンドモデルに追加
* グラウンドコントローラーの`index`アクションにおいてscopeを用いてグラウンドデータの全件取得をするように修正

## 関連チケット
[KIRYU_DIGITAL-24](https://sporture1.backlog.jp/view/KIRYU_DIGITAL-24)

## 参考
## 公開設定を表示にした際の挙動

- グラウンド一覧画面で表示されていることを確認 
    

https://github.com/dx-works/910kiryu/assets/58897760/0a471ac8-0a71-498b-abab-635845f84488



## 公開設定を非表示にした際の挙動

 - グラウンド一覧画面で表示されていないことを確認 

https://github.com/dx-works/910kiryu/assets/58897760/ae330432-75bb-4fd9-93f8-4f983eff281e

## 公開設定が表示・非表示に関わらず日程・結果画面において球場名が表示されていること

 - 公開設定が表示の球場11が日程・結果画面に表示されており、公開設定を非公開に更新しても変わらずに画面に表示されることを確認
   

https://github.com/dx-works/910kiryu/assets/58897760/8c647a17-ea21-48a5-96b3-e741ca537e22

## 共有
[【CMS】単体テスト・球場](https://docs.google.com/spreadsheets/d/1P84n1Mj1ZhdDw9PWP7BYCP6RnEZgab-zm7cZiWpZa2A/edit#gid=1692757351)

