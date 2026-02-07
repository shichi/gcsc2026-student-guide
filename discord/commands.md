# Discord Bot Commands

GCSC2026 Discord Botのコマンド一覧

---

## 🤖 About the Bot

**Bot Name:** GCSC2026 Community Manager

このBotは、GCSC2026イベントを円滑に運営するための様々な機能を提供します。

---

## 📝 Self-Introduction Commands

### `/set_intro`

自己紹介を登録します。

**使用場所:** 任意のチャンネル

**例:**
```
/set_intro
```

モーダルフォームが表示され、以下を入力できます：
- 名前
- 大学
- 専攻
- 趣味・興味
- このイベントへの期待

登録後、`#introductions` チャンネルに自動的に投稿されます。

---

## 👥 Mentor Booking Commands

メンター予約システムのコマンド。**チームチャンネルでのみ使用可能**。

### `/mentor ui` ⭐ **推奨**

インタラクティブUIでメンターを予約します。

**使用場所:** `#team-01` 〜 `#team-20`

**使い方:**
1. `/mentor ui` を実行
2. セッションを選択
3. タイムスロットを選択
4. メンターを選択
5. 確認して予約完了

**特徴:**
- ドロップダウンで簡単選択
- 予約済みメンターは自動的に除外
- 戻るボタンで修正可能

### `/mentor book`

ダイレクト予約（上級者向け）

**使用場所:** `#team-01` 〜 `#team-20`

**パラメータ:**
- `session` - セッション名（`session_1`, `session_2`, `session_3`）
- `timeslot` - タイムスロット（例: `10:00-10:20`）
- `mentor` - メンター名（アルファベット）

**例:**
```
/mentor book session:session_1 timeslot:10:00-10:20 mentor:Masatoshi KANEKO
```

### `/mentor cancel`

予約をキャンセルします。

**使用場所:** `#team-01` 〜 `#team-20`

**パラメータ:**
- `session` - セッション名
- `timeslot` - タイムスロット

**例:**
```
/mentor cancel session:session_1 timeslot:10:00-10:20
```

### `/mentor my`

自分のチームの予約を確認します。

**使用場所:** `#team-01` 〜 `#team-20`

**例:**
```
/mentor my
```

予約している全セッションの情報が表示されます。

### `/mentor status`

セッション全体の予約状況を確認します。

**使用場所:** 任意のチャンネル

**パラメータ:**
- `session` - セッション名（`session_1`, `session_2`, `session_3`）

**例:**
```
/mentor status session:session_1
```

各タイムスロットの予約状況が一覧表示されます。

---

## 🎯 Team Formation Commands

### `/register_team`

チームメンバーを登録します。

**権限:** スタッフのみ

**使用場所:** 任意のチャンネル

### `/team_status`

チーム編成状況を確認します。

**権限:** スタッフのみ

---

## 📢 Announcement Commands

### `/announce`

全体アナウンスを送信します。

**権限:** 運営スタッフのみ

### `/announce_file`

ファイル付きアナウンスを送信します。

**権限:** 運営スタッフのみ

---

## 📊 Statistics Commands

### `/intro_stats`

自己紹介の統計情報を表示します。

**使用場所:** 任意のチャンネル

**例:**
```
/intro_stats
```

- 自己紹介済み人数
- 国別内訳
- 興味・趣味の統計

### `/my_intro`

自分の自己紹介を確認します。

**使用場所:** 任意のチャンネル

**例:**
```
/my_intro
```

---

## ⚙️ Server Setup Commands

### `/setup_server`

サーバーの初期設定を行います。

**権限:** 管理者のみ

**機能:**
- チャンネル作成
- ロール設定
- 権限設定

### `/create_invite`

招待リンクを作成します。

**権限:** スタッフのみ

---

## 💡 Command Tips

### 1. コマンドの自動補完

`/` を入力すると、利用可能なコマンドが表示されます。

### 2. パラメータのヒント

コマンドを選択すると、必要なパラメータが表示されます。

### 3. エラーメッセージ

エラーが発生した場合、赤い文字でエラーメッセージが表示されます。内容を確認して再試行してください。

### 4. プライベート応答

一部のコマンド（`/mentor my` など）は、あなたにのみ表示される応答を返します（ephemeral）。

---

## 🔍 Command Permissions

| コマンド | 誰が使える？ |
|---------|------------|
| `/set_intro` | 全員 |
| `/mentor ui` | チームメンバー（チームチャンネル内） |
| `/mentor book` | チームメンバー（チームチャンネル内） |
| `/mentor cancel` | チームメンバー（チームチャンネル内） |
| `/mentor my` | チームメンバー（チームチャンネル内） |
| `/mentor status` | 全員 |
| `/intro_stats` | 全員 |
| `/my_intro` | 全員 |
| `/register_team` | スタッフのみ |
| `/announce` | 運営スタッフのみ |
| `/setup_server` | 管理者のみ |

---

## ❓ Troubleshooting

### コマンドが表示されない

1. サーバーに正しく参加しているか確認
2. Discordを再起動
3. ブラウザ版の場合、キャッシュをクリア

### コマンドが実行できない

1. 正しいチャンネルで実行しているか確認
   - 例: `/mentor` コマンドはチームチャンネルでのみ使用可能
2. パラメータが正しく入力されているか確認
3. エラーメッセージを確認

### Bot が応答しない

1. Botがオンラインか確認（メンバーリストで確認）
2. 数分待ってから再試行
3. それでも解決しない場合は運営スタッフに連絡

---

## 🆕 Coming Soon

今後追加予定の機能：
- チーム内投票機能
- リマインダー機能
- プロジェクト進捗トラッキング

---

[← Back to Discord Guide](README.md) | [Getting Started Guide](getting-started.md)
