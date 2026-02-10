---
name: threads
description: "Threads content agent. Use when user asks about Threads posts, hooks, content plan, strategy, copywriting, engagement, analytics. Activates on: 'threads post', 'write for threads', 'threads strategy', 'threads hook', 'threads пост', 'напиши для threads', 'threads стратегия', 'threads хук'."
---

# Threads Content Agent

Full content cycle for Meta Threads: from strategy to a million followers.

## Core Principle

```
Threads = Reach → Telegram = Sales
```

Threads for building free audience, Telegram for monetization.

---

## File Router

When requested, load the corresponding reference file:

| Request contains | File |
|------------------|------|
| strategy, positioning, ToV, voice, funnel, monetization | [threads-strategy.md](threads-strategy.md) |
| research, audience, competitors, analysis, patterns | [threads-research.md](threads-research.md) |
| content plan, categories, calendar, frequency, schedule | [threads-content-plan.md](threads-content-plan.md) |
| hook, first line, opener, headline | [threads-hooks.md](threads-hooks.md) |
| post, text, copywriting, formula, structure, CTA | [threads-copywriting.md](threads-copywriting.md) |
| engagement, comments, DM, community | [threads-engagement.md](threads-engagement.md) |
| metrics, analytics, KPI, results, reach | [threads-analytics.md](threads-analytics.md) |

---

## Workflow: Full Cycle

```
1. Research → threads-research.md
   - Niche and competitor analysis
   - Target audience definition
   - Study viral posts

2. Strategy → threads-strategy.md
   - Hard vs Soft niche
   - Positioning and ToV
   - Monetization funnel

3. Content Plan → threads-content-plan.md
   - Categories by niche type
   - Content calendar
   - Posting frequency (3-5/day)

4. Writing → threads-copywriting.md + threads-hooks.md
   - Hook (spend 50% of time on it!)
   - Post structure
   - CTA in pinned comment

5. Engagement → threads-engagement.md
   - Commenting (10-20/day)
   - Reply to comments (first 30-60 min are critical)
   - Transfer to Telegram

6. Analytics → threads-analytics.md
   - Track metrics
   - Analyze top posts
   - Optimize strategy
```

---

## Quick Actions

| Command | Action | Files |
|---------|--------|-------|
| "threads post on topic X" | Generate post with hook and CTA | hooks + copywriting |
| "threads plan for the week" | 7-day content plan | content-plan |
| "threads analyze @username" | Competitor analysis | research |
| "threads strategy for [niche]" | Full strategy | strategy |
| "threads hooks on topic X" | 5-10 hook variations | hooks |
| "how to grow account" | Growth plan | strategy + content-plan |

---

## Context Loading

При генерации контента загрузи из проекта:

1. `projects/{project}/brand/voice-style.md` — как писать
2. `projects/{project}/learning/patterns.md` — что работает
3. `projects/{project}/learning/examples/threads/` — референсы

**Используй примеры пользователя как образец стиля.**

---

## Key Rules

### Algorithms
- Time on post — main metric (like YouTube)
- First 30-60 minutes are critical for reach
- Thread can go viral for up to 2 days
- 1 out of 3 posts usually takes off
- Account warm-up: 5-14 days

### Content
- Hook — most important (first line visible in feed)
- 500 characters max per thread
- Links ONLY in pinned comment!
- Only OPEN Telegram links
- Image: friendly expert that people want to rely on

### Content Types by Effectiveness
1. Questions (for warm-up)
2. Like-posts / Wishes (for reach)
3. Stories / Internal conflict (for trust)
4. Results with emotions (for hard niches)
5. Astrology / Cards (gold for soft niches)

### Frequency
- Minimum: 1-2 posts/day
- Optimal: 3-5 posts/day
- Don't skip days — reach drops!

---

## Platform Specifics

- Threads linked to Instagram (profile from IG)
- Text format, up to 500 characters per thread
- Video up to 5 minutes, images increase conversion
- Hashtags don't work — keywords do
- Instagram algorithms, but platform is in early stage

---

## Notes

- GPT doesn't understand humor well — write humor yourself
- Update lead magnets every 1-2 weeks (they burn out)
- Don't open Threads when upset — you'll write something regrettable

---

## Learning Integration

### Где искать паттерны

| Источник | Путь |
|----------|------|
| **Global** | `.claude/skills/threads/` |
| **Project** | `projects/{project}/learning/skill-learning/threads/patterns.md` |
| **Anti-patterns** | `projects/{project}/learning/skill-learning/threads/anti-patterns.md` |
| **Examples** | `projects/{project}/learning/skill-learning/threads/examples/` |

### Команды обучения

| Команда | Куда пишет |
|---------|-----------|
| `это сработало: [что]` | `skill-learning/threads/patterns.md` |
| `это не сработало: [что]` | `skill-learning/threads/anti-patterns.md` |
| `запомни пример: [пост]` | `skill-learning/threads/examples/` |

---

## Critics System

После генерации поста — 3 критика.

### Hook Expert
- ✅ Первая строка = интрига
- ✅ Конкретика или число
- ❌ Вода, общие слова

### Engagement Expert
- ✅ Провокация мнения
- ✅ Призыв к диалогу
- ❌ Назидательный тон

### Conversion Expert
- ✅ CTA в закрепе
- ✅ Мягкий переход к лид-магниту
- ❌ Ссылка в теле поста

---

*Threads Skill v1.1 — Learning + Critics*
