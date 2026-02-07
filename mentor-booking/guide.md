# Mentor Booking System Guide

メンター予約システムの使い方

---

## 📋 System Overview

GCSC2026のメンター予約は**20分単位のタイムスロット制**を採用しています。

### タイムスロットの特徴
- 各2時間セッションを**6つの20分スロット**に分割
- チームは各セッションで**複数のタイムスロット**を予約可能（ただし連続不可）
- 各メンターは1つのタイムスロットで**1チームのみ**対応
- Discord上で簡単に予約・キャンセル可能

---

## 📅 Available Sessions

| セッション | 時間 | タイムスロット数 |
|-----------|------|-----------------|
| **Session 1** | 10:00-12:00 | 6スロット（各20分） |
| **Session 2** | 13:00-15:00 | 6スロット（各20分） |
| **Session 3** | 15:00-17:00 | 6スロット（各20分） |
| **Faculty Night** | 20:00-22:00 | 予約不可（教員巡回） |

---

## 💬 Discord Commands

### 1. インタラクティブUI予約（推奨）

チームチャンネル（`#team-01`〜`#team-20`）で：

```
/mentor ui
```

実行すると、ステップバイステップで予約できるUIが表示されます：

1. **セッション選択** → ドロップダウンから選択
2. **タイムスロット選択** → 利用可能な時間帯を選択
3. **メンター選択** → 予約可能なメンターを選択
4. **確認** → 予約内容を確認して確定

### 2. ダイレクト予約（上級者向け）

```
/mentor book session:session_1 timeslot:10:00-10:20 mentor:Masatoshi KANEKO
```

**パラメータ:**
- `session` - セッション名（`session_1`, `session_2`, `session_3`）
- `timeslot` - タイムスロット（例：`10:00-10:20`）
- `mentor` - メンター名（アルファベット表記）

### 3. 予約をキャンセル

```
/mentor cancel session:session_1 timeslot:10:00-10:20
```

### 4. 自分のチームの予約確認

```
/mentor my
```

自分のチームが予約したタイムスロットとメンターが一覧表示されます。

### 5. セッション全体の予約状況確認

```
/mentor status session:session_1
```

指定したセッションの全タイムスロットの予約状況を確認できます。

---

## 👥 Available Mentors

### Session 1: 10:00-12:00

**Timeslots:** 10:00-10:20, 10:20-10:40, 10:40-11:00, 11:00-11:20, 11:20-11:40, 11:40-12:00

**Mentors:**
- **Masatoshi KANEKO** (金子 匡俊) - Room 406
- **Julian Brody** - Room 407
- **Heedong YOO** - Room 410
- **Hyun Joo CHUNG** - Room 411

### Session 2: 13:00-15:00

**Timeslots:** 13:00-13:20, 13:20-13:40, 13:40-14:00, 14:00-14:20, 14:20-14:40, 14:40-15:00

**Mentors:**
- **Kenta MURAOKA** (村岡 健太) - Room 406
- **Keiichiro KATAOKA** (片岡 慶一郎) - Room 407
- **Seung Hwan MOK** - Room 410
- **Hyun Joo CHUNG** - Room 411

### Session 3: 15:00-17:00

**Timeslots:** 15:00-15:20, 15:20-15:40, 15:40-16:00, 16:00-16:20, 16:20-16:40, 16:40-17:00

**Mentors:**
- **Kenta MURAOKA** (村岡 健太) - Room 406
- **Takatsugu KONNO** (紺野 貴嗣) - Room 407
- **Seung Hwan MOK** - Room 410
- **Hyun Joo CHUNG** - Room 411

### Faculty Night: 20:00-22:00

**Not available for booking** - Faculty members will circulate among teams to provide support.

---

## ⚠️ Important Rules

1. **同じセッション内で複数予約可能**: 各チームは1つのセッション内で複数のタイムスロットを予約できます
   - ✅ 例: Session 1の10:00-10:20と10:40-11:00を予約（OK）
   - ❌ 例: Session 1の10:00-10:20と10:20-10:40を予約（NG - 連続）

2. **連続するタイムスロットはNG**: 同じセッション内で連続するタイムスロット（例：10:00-10:20と10:20-10:40）の予約はできません
   - 少なくとも1つのタイムスロットを空ける必要があります

3. **同じタイムスロットで重複予約はNG**: 同じタイムスロットで同じメンターを複数のチームが予約することはできません

4. **先着順**: 予約は先着順。人気のあるメンター・時間帯は早めに予約を

5. **アルファベット入力**: メンター名はアルファベット表記で入力（例：`Masatoshi KANEKO`）
   - インタラクティブUI (`/mentor ui`) なら選ぶだけでOK

6. **Faculty Nightは予約不可**: 20:00-22:00のFaculty Nightは教員が各チームを巡回します

---

## 📊 Check Booking Status

### GitHub上での確認

全体の予約状況はGitHub上でリアルタイムに更新されます：

**予約状況URL**: [mentor-booking/schedule.md](schedule.md)

### Discord上での確認

- `/mentor my` - 自チームの予約を確認
- `/mentor status session:session_1` - セッション全体の状況を確認

---

## ❓ FAQ

### Q1: 同じセッションで複数のメンターを予約できますか？

**A:** はい、可能です。1つのセッション内で複数のタイムスロットを予約できます。ただし、**連続するタイムスロットの予約はできません**。少なくとも1つのタイムスロットを空ける必要があります。

**例:**
- ✅ OK: Session 1の10:00-10:20 (Mentor A) と 10:40-11:00 (Mentor B)
- ❌ NG: Session 1の10:00-10:20 (Mentor A) と 10:20-10:40 (Mentor B) ← 連続

### Q2: 異なるセッションで同じメンターを予約できますか？

**A:** はい、可能です。Session 1、Session 2、Session 3はそれぞれ独立しているため、異なるセッションであれば同じメンターを予約できます。

### Q3: 予約後に時間を変更したい場合は？

**A:** 一度 `/mentor cancel` で予約をキャンセルしてから、新しいタイムスロットで `/mentor book` または `/mentor ui` を実行してください。

### Q4: メンター名の入力が難しいです

**A:** `/mentor ui` コマンドを使えば、ドロップダウンから選ぶだけで予約できます。ダイレクト予約の場合は、コピー＆ペーストも利用できます。

### Q5: Faculty Nightはどうすれば予約できますか？

**A:** Faculty Night（20:00-22:00）は予約制ではありません。教員が各チームを巡回してサポートを提供します。

---

## 💡 Tips for Effective Mentoring

- **事前準備**: メンタリング前にチーム内で質問事項を整理しておく
- **20分を有効活用**: 時間が限られているため、要点を絞って相談する
- **複数セッション活用**: 1つのセッションだけでなく、複数のセッションでメンターを予約することも検討
- **異なる視点**: 異なるバックグラウンドのメンターに相談し、多様な視点を得る

---

**Good luck with your project! 🚀**

[← Back to Mentor Booking](README.md) | [Check Current Schedule →](schedule.md)
