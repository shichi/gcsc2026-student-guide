# Mentor Booking System Guide (English)

[🇯🇵 日本語](guide.ja.md) | [🇰🇷 한국어](guide.ko.md)

---

## 📋 System Overview

GCSC2026's mentor booking system uses **20-minute timeslots**.

### Timeslot Features
- Each 2-hour session is divided into **six 20-minute slots**
- Teams can book **multiple timeslots** per session (but not consecutive)
- Each mentor handles **one team per timeslot**
- Easy booking and cancellation via Discord

---

## 📅 Available Sessions

| Session | Time | Number of Timeslots |
|---------|------|---------------------|
| **Session 1** | 10:00-12:00 | 6 slots (20 min each) |
| **Session 2** | 13:00-15:00 | 6 slots (20 min each) |
| **Session 3** | 15:00-17:00 | 6 slots (20 min each) |
| **Faculty Night** | 20:00-22:00 | No booking (faculty circulates) |

---

## 💬 Discord Commands

### 1. Interactive UI Booking (Recommended)

In your team channel (`#team-01` to `#team-20`):

```
/mentor ui
```

This displays a step-by-step UI for booking:

1. **Select Session** → Choose from dropdown
2. **Select Timeslot** → Choose available time
3. **Select Mentor** → Choose available mentor
4. **Confirm** → Review and confirm booking

### 2. Direct Booking (Advanced)

```
/mentor book session:session_1 timeslot:10:00-10:20 mentor:Masatoshi KANEKO
```

**Parameters:**
- `session` - Session name (`session_1`, `session_2`, `session_3`)
- `timeslot` - Timeslot (e.g., `10:00-10:20`)
- `mentor` - Mentor name (alphabetic format)

### 3. Cancel Booking

```
/mentor cancel session:session_1 timeslot:10:00-10:20
```

### 4. Check Your Team's Bookings

```
/mentor my
```

Displays all timeslots and mentors your team has booked.

### 5. Check Session Booking Status

```
/mentor status session:session_1
```

View booking status for all timeslots in the specified session.

---

## 👥 Available Mentors

### Session 1: 10:00-12:00

**Timeslots:** 10:00-10:20, 10:20-10:40, 10:40-11:00, 11:00-11:20, 11:20-11:40, 11:40-12:00

**Mentors:**
- **Masatoshi KANEKO** (金子 匡俊) - Room 406
- **Ayame ITO** (伊藤 あやめ / Pollimill CEO) - Room 407
- **Heedong YOO** - Room 410
- **Hyun Joo CHUNG** - Room 411
- **Kenta MURAOKA** (村岡 健太 / EY) - Room 406 *NEW*

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

1. **Multiple bookings per session allowed**: Teams can book multiple timeslots within one session
   - ✅ Example: Book 10:00-10:20 and 10:40-11:00 in Session 1 (OK)
   - ❌ Example: Book 10:00-10:20 and 10:20-10:40 in Session 1 (NG - consecutive)

2. **No consecutive timeslots**: You cannot book consecutive timeslots within the same session (e.g., 10:00-10:20 and 10:20-10:40)
   - Must leave at least one timeslot gap

3. **No duplicate bookings**: Multiple teams cannot book the same mentor in the same timeslot

4. **First come, first served**: Bookings are on a first-come basis. Popular mentors and times fill up quickly

5. **Alphabetic input**: Enter mentor names in alphabetic format (e.g., `Masatoshi KANEKO`)
   - Using interactive UI (`/mentor ui`) lets you simply select from a dropdown

6. **Faculty Night not bookable**: 20:00-22:00 Faculty Night has faculty members circulating among teams

---

## 📊 Check Booking Status

### On GitHub

Overall booking status is updated in real-time on GitHub:

**Booking Status URL**: [mentor-booking/schedule.md](schedule.md)

### On Discord

- `/mentor my` - Check your team's bookings
- `/mentor status session:session_1` - Check overall session status

---

## ❓ FAQ

### Q1: Can I book multiple mentors in the same session?

**A:** Yes, you can. You can book multiple timeslots within one session. However, **you cannot book consecutive timeslots**. You must leave at least one timeslot gap.

**Examples:**
- ✅ OK: Session 1's 10:00-10:20 (Mentor A) and 10:40-11:00 (Mentor B)
- ❌ NG: Session 1's 10:00-10:20 (Mentor A) and 10:20-10:40 (Mentor B) ← consecutive

### Q2: Can I book the same mentor in different sessions?

**A:** Yes, you can. Session 1, Session 2, and Session 3 are independent, so you can book the same mentor in different sessions.

### Q3: What if I want to change the time after booking?

**A:** First cancel your booking with `/mentor cancel`, then make a new booking with `/mentor book` or `/mentor ui` for the new timeslot.

### Q4: Entering mentor names is difficult

**A:** Using the `/mentor ui` command lets you simply select from a dropdown. For direct booking, you can also copy and paste names.

### Q5: How do I book Faculty Night?

**A:** Faculty Night (20:00-22:00) is not a booking system. Faculty members will circulate among teams to provide support.

---

## 💡 Tips for Effective Mentoring

- **Prepare in advance**: Organize your questions within the team before mentoring
- **Use 20 minutes effectively**: Time is limited, so focus on key points for discussion
- **Use multiple sessions**: Consider booking mentors across multiple sessions, not just one
- **Get diverse perspectives**: Consult mentors with different backgrounds to gain various viewpoints

---

**Good luck with your project! 🚀**

[← Back to Mentor Booking](README.md) | [Check Current Schedule →](schedule.md)
