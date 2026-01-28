# FieldTrain — Vibe Coding Spec

*Use this to prompt your AI app builder*

---

## One-Liner
Gamified training app where companies upload docs and AI creates quizzes for field staff.

---

## Two User Types

### 1. Admin (Back Office)
- Upload training content (PDF/text)
- View staff progress & scores
- See leaderboards
- Download completion reports

### 2. Staff (Field Worker - Mobile)
- Take quizzes on phone
- See leaderboard ranking
- View completed quizzes & scores
- Download certificates

---

## MVP Screens

### Admin Web Dashboard
1. **Login**
2. **Dashboard** — Overview stats (total staff, completion rates, top performers)
3. **Content** — Upload PDFs/docs, see list of uploaded content
4. **Quizzes** — List of AI-generated quizzes, preview questions
5. **Staff** — List of users, invite new, see individual progress
6. **Leaderboard** — Company-wide rankings
7. **Reports** — Export completion data

### Staff Mobile App
1. **Login**
2. **Home** — Available quizzes, quick stats
3. **Quiz** — Take quiz (multiple choice, 5-10 questions)
4. **Results** — Score, correct answers, certificate button
5. **Leaderboard** — See ranking vs peers
6. **Profile** — Completed quizzes, certificates, total points

---

## Core Flow

### Admin Flow
```
Upload PDF → AI processes → Quiz generated → Assign to staff → Track completions
```

### Staff Flow
```
Get notification → Open app → Take quiz → See score → Check leaderboard → Get certificate
```

---

## Quiz Format
- 5-10 multiple choice questions per quiz
- Generated from uploaded content
- Immediate feedback after each question
- Pass threshold: 70% (configurable)
- Can retake to improve score

---

## Gamification Elements
- **Points** — Earn per quiz completed
- **Leaderboard** — Weekly rankings
- **Certificates** — PDF generated on pass

---

## Data Model (Simple)

```
Company
  - id, name, logo

User
  - id, company_id, name, email, role (admin/staff)

Content
  - id, company_id, title, file_url, uploaded_at

Quiz
  - id, content_id, title, questions (JSON)

QuizAttempt
  - id, user_id, quiz_id, score, completed_at

Certificate
  - id, attempt_id, pdf_url
```

---

## Tech Suggestions
- **Mobile:** React Native or Flutter (cross-platform)
- **Backend:** Supabase or Firebase (fast to build)
- **AI:** OpenAI API for quiz generation
- **PDF Processing:** pdf-parse or similar
- **Certificates:** Generate PDF with jsPDF or similar

---

## Prompt for Vibecode/AI Builder

```
Build a gamified training app called FieldTrain.

Two user types:
1. Admin (web) - uploads training documents, tracks staff progress
2. Staff (mobile) - takes quizzes, sees leaderboard, earns certificates

Core features:
- Admin uploads PDF/documents
- AI reads content and generates multiple choice quizzes (5-10 questions)
- Staff takes quizzes on mobile app
- Leaderboard shows rankings by score/points
- Certificate PDF generated when quiz passed
- Admin dashboard shows completion tracking

Keep it simple - MVP only. Mobile-first for staff, web dashboard for admin.
```

---

## What to Build First (Priority)

1. **Staff mobile quiz experience** — This is the core value
2. **Basic admin upload** — Get content in
3. **AI quiz generation** — The magic
4. **Leaderboard** — Gamification hook
5. **Certificates** — Compliance proof

---

*Ready to vibe code! 🛠️*
