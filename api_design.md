# API設計
各APIの使用には, HTTPヘッダに `Authorization: Bearer <access_token>` 形式でのアクセストークンの指定が必須となっている.  
アクセストークンは, 認証系APIの `/api/v1/auth/register` 又は `/api/v1/auth/login` によって発行される.

- [認証系API](./api_design/auth.md)
- [ユーザー系API](./api_design/user.md)
- [投稿系API](./api_design/post.md)
- [タイムライン系API](./api_design/timeline.md)
- [通知系API](./api_design/notice.md)
- [報告系API](./api_design/report.md)
- [失敗時のステータス](./api_design/failure.md)