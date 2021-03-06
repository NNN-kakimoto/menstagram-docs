### エラー時のレスポンス

##### パターン１

リクエストの各パラメータに対して個別にエラーメッセージが設定されるパターン.

```json
{
    "errors": {
        "user_id": [
            "XXXX",
            "XXXX"
        ],
        "password": [
            "XXXX",
            "XXXX"
        ]
    }
}
```

##### パターン２

リクエスト全体で１つのメッセージが設定されるパターン.

```json
{
    "errors": {
        "message": "XXXX"
    }
}
```

### エラー時のステータス

##### リクエストの形式が不正

- リクエストのパラメータが誤っている場合など

```
400 Bad Request
```

##### 認証されていない

- 認証が必要なAPIでアクセストークン無しでアクセスした場合など

```
401 Uuauthorized
```

##### 禁止されている

- リソースへの権限がない場合など

```
403 Forbidden
```

##### リソースが存在しない

- 存在しないスラープをリクエストした場合など

```
404 Not Found
```