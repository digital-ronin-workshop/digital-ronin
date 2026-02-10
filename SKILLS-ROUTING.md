# Skills Routing

> Компактная таблица skills → paths для Claude

---

## Skills Table

| Skill | Trigger Keywords | Files to Load |
|-------|------------------|---------------|
| **threads** | "threads", "threads post", "пост" | `.claude/skills/threads/` |
| **youtube** | "youtube", "youtube script", "сценарий" | `.claude/skills/youtube/` |
| **reels** | "reels", "shorts", "tiktok" | `.claude/skills/reels/` |
| **carousel** | "carousel", "карусель" | `.claude/skills/carousel/` + `.claude/skills/nano-banana/` |
| **telegram** | "telegram", "тг пост", "tg post" | `.claude/skills/telegram/` |
| **selling-meanings** | Auto: "продающий", "оффер", "CTA" | `.claude/skills/selling-meanings/` |
| **storytelling** | Auto: "история", "story", "кейс" | `.claude/skills/storytelling/` |
| **launch** | "launch", "запуск", "PLF", "прогрев" | `.claude/skills/launch/` |
| **nano-banana** | "image prompt", "картинка", "обложка" | `.claude/skills/nano-banana/` |
| **prompt-engineer** | "create prompt", "improve prompt" | `.claude/skills/prompt-engineer/` |
| **skill-creator** | "create skill", "new skill" | `.claude/skills/skill-creator/` |
| **agent-architect** | "создай агента", "new agent" | `.claude/skills/agent-architect/` |
| **learning-processor** | "обработай", "обучи" | `.claude/skills/learning-processor/` |

---

## Auto-Loading Rules

### selling-meanings (Auto-loads for selling content)

**Keywords:**
- "продающий", "selling", "оффер", "offer"
- "CTA", "закреп", "pinned"
- "конверсия", "продажи"

### storytelling (Auto-loads for story content)

**Keywords:**
- "история", "story", "кейс", "case"
- "сторителлинг", "storytelling"

---

## Skill Combinations

| Content Type | Skills |
|--------------|--------|
| Продающая карусель | carousel + selling-meanings + nano-banana |
| Threads запуск | threads + launch + selling-meanings |
| YouTube история | youtube + storytelling |
| Selling Threads | threads + selling-meanings |

---

## Usage

**When user triggers format:**
1. Match trigger → find skill
2. Load files from skill folder
3. Check auto-loading (selling-meanings, storytelling)
4. Load project context (brand/, learning/)

**Example:**
```
User: "продающий пост"
    ↓
Skills:
1. threads (format)
2. selling-meanings (auto: "продающий")
    ↓
Files:
- .claude/skills/threads/
- .claude/skills/selling-meanings/
```

---

*Skills Routing v2.0 — Content Factory*
