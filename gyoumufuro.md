@startuml
ユーザ -> webサーバ : ログイン
webサーバ -> DBサーバ : ログイン照会
DBサーバ -> DBサーバ : ログイン処理
DBサーバ -> webサーバ : 認証結果
activate ユーザ
alt 認証成功
webサーバ -> ユーザ : ユーザ名表示
else 認証失敗
webサーバ -> ユーザ : 失敗メッセージ表示
end
ユーザ -> webサーバ : カートに追加
webサーバ -> DBサーバ : カート更新
DBサーバ -> DBサーバ : カート更新処理
DBサーバ -> webサーバ : 結果
webサーバ -> ユーザ : 表示
ユーザ -> webサーバ : カートclick
webサーバ -> ユーザ : 表示
deactivate ユーザ
@enduml
