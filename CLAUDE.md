# Content Factory

> AI-ассистент для создания контента. Пишет в твоём голосе.

---

## Первый раз?

Напиши:

**начать** или **/setup**

За 10 минут:
1. Узнаю про тебя и твой бизнес
2. Настрою голос и стиль
3. Сгенерирую первые посты

---

## Быстрые команды

| Слово | Слэш | Что делает |
|-------|------|------------|
| `начать` | `/setup` | Первая настройка (интервью + первые посты) |
| `threads 5` | `/threads 5` | 5 постов для Threads |
| `youtube script [тема]` | `/youtube script` | Сценарий для YouTube |
| `carousel [тема]` | `/carousel` | Карусель для Instagram |

---

## Как это работает

```
Skills (методы) + Твой голос (brand/) = Твой контент
```

**Skills** — универсальные методики: как писать хуки, структурировать посты, вовлекать аудиторию.

**Твой голос** — файлы в `brand/`: кто ты, как говоришь, кто твои клиенты.

Claude загружает нужный skill + твой голос → генерирует контент в твоём стиле.

---

## Структура проекта

```
твой-проект/
├── brand/                # Твой голос (заполняется при "начать")
│   ├── profile.md       # Кто ты
│   ├── voice-style.md   # Как говоришь
│   └── audience.md      # Кто клиенты
│
├── learning/            # Система обучения
│   ├── approved-patterns.md  # Что работает
│   └── anti-patterns.md      # Что не работает
│
└── content/             # Черновики и готовый контент
```

---

## Команды обучения

Система учится твоему стилю в процессе работы:

| Слово | Что делает |
|-------|------------|
| `это сработало` | Сохранить как успешный паттерн |
| `это не сработало` | Запомнить как анти-паттерн |
| `запомни стиль: [что]` | Обновить голос |

---

## Все команды

### Контент

| Слово | Описание |
|-------|----------|
| `threads [N]` | N постов для Threads |
| `youtube script [тема]` | Сценарий для YouTube |
| `youtube shorts [тема]` | Короткое видео (до 60 сек) |
| `carousel [тема]` | Карусель для Instagram |
| `reels [тема]` | Рилс для Instagram |
| `telegram [тема]` | Пост для Telegram |

### Настройка

| Слово | Слэш | Описание |
|-------|------|----------|
| `начать` | `/setup` | Первая настройка проекта |
| `интервью` | `/interview` | Полное интервью (7 блоков, 20-30 мин) |
| `интервью мини` | `/interview mini` | Быстрое интервью (3 вопроса, 10 мин) |

### Анализ

| Слово | Описание |
|-------|----------|
| `разбери [скриншот]` | Анализ поста по скриншоту |
| `инсайты` | Что сработало, что нет |
| `критика` | Оценка от 3 критиков (Sales, Creative, Structure) |

---

## Документация

### Для людей (простым языком)
- [Что такое скиллы?](docs/skills-guide.md) — 12 методик создания контента
- [Что такое агенты?](docs/agents-guide.md) — твоя команда специалистов

### Техническое
- [Полный гайд установки](docs/00-complete-setup-guide.md)
- [Установка Claude Code](docs/01-installation.md)
- [Первый пост за 30 минут](docs/02-first-post.md)
- [Интеграции (Notion, n8n)](docs/03-integrations.md)

---

## FAQ

**Q: Как изменить голос?**
A: Отредактируй `brand/voice-style.md` или скажи `запомни стиль: [что изменить]`

**Q: Как добавить новый формат?**
A: Форматы уже включены. Используй: `threads`, `youtube`, `carousel`, `reels`, `telegram`

**Q: Посты не похожи на меня?**
A: Скажи `интервью` заново или добавь примеры в `learning/approved-patterns.md`

**Q: Как подключить Notion?**
A: См. [docs/03-integrations.md](docs/03-integrations.md)

---

## Техническое

### Skills — Автоматическая загрузка

Все скиллы лежат в `.claude/skills/`. Claude загружает нужные автоматически по триггеру.

| Скилл | Путь | Триггер | Что делает |
|-------|------|---------|------------|
| **threads** | `threads/SKILL.md` + `threads-copywriting.md` + `threads-hooks.md` | "threads", "пост", "тред" | Методика Threads: VISP, хуки, вовлечение |
| **telegram** | `telegram/SKILL.md` + `telegram-copywriting.md` + `telegram-hooks.md` | "telegram", "телеграм", "тг пост" | Методика Telegram: хуки, копирайтинг |
| **youtube** | `youtube/SKILL.md` + нужные модули | "youtube", "сценарий", "script" | YouTube методика: VHF, TOP-5, удержание |
| **carousel** | `carousel/SKILL.md` + `carousel-structure.md` + `carousel-types.md` | "carousel", "карусель" | Структура каруселей, дизайн, CTA |
| **reels** | `reels/SKILL.md` + `reels-methodology.md` | "reels", "shorts", "рилс" | VISP формула, вертикальное видео |
| **selling-meanings** | `selling-meanings/SKILL.md` + нужный модуль | "продающий", "оффер", "CTA", "смыслы" | Продающие смыслы, формулы, психология |
| **storytelling** | `storytelling/SKILL.md` + `slippery-slide.md` | "история", "story", "кейс" | Сторителлинг, скользкая горка, триггеры |
| **nano-banana** | `nano-banana/SKILL.md` + нужный модуль | "картинка", "обложка", "промпт" | Генерация изображений, identity kit |
| **heygen** | `heygen/SKILL.md` + `heygen-rules.md` + `heygen-motion.md` | "heygen", "аватар", "видео аватар" | AI-аватары, правила озвучки |
| **launch** | `launch/SKILL.md` | "запуск", "прогрев", "launch" | Запуски, воронки, прогревы |
| **prompt-engineer** | `prompt-engineer/SKILL.md` | "промпт", "prompt" | Промпт-инженерия |
| **learning-processor** | `learning-processor/SKILL.md` | "обучение", "разобрать материал" | Извлечение знаний из материалов |
| **DigitalRonin** | `projects/DigitalRonin/CLAUDE.md` | "DigitalRonin", "Ronin" | Проект DigitalRonin |

### Модули selling-meanings (загружать по задаче)

| Задача | Модуль |
|--------|--------|
| Вытащить смыслы из текста | `selling-meanings/extraction.md` |
| Усилить текст продающими элементами | `selling-meanings/amplification.md` |
| Формулы копирайтинга (PAS, AIDA, etc) | `selling-meanings/formulas.md` |
| Офферы по Хормози | `selling-meanings/hormozi-offers.md` |
| Психология продаж | `selling-meanings/psychology.md` |
| Готовые шаблоны | `selling-meanings/templates.md` |

### Модули storytelling (загружать по задаче)

| Задача | Модуль |
|--------|--------|
| Скользкая горка (затягивающий текст) | `storytelling/slippery-slide.md` |
| Психологические триггеры | `storytelling/psychological-triggers.md` |
| Продающая статья | `storytelling/selling-article.md` |

### Общие паттерны (shared-learnings)

| Файл | Назначение |
|------|------------|
| `shared-learnings/UNIVERSAL-APPROVED-PATTERNS.md` | Что работает (все форматы) |
| `shared-learnings/UNIVERSAL-ANTI-PATTERNS.md` | Что НЕ работает |
| `shared-learnings/TONE-FORMULAS.md` | Формулы тона |
| `shared-learnings/SOURCES.md` | Источники знаний |

### Порядок загрузки

```
1. РОУТИНГ  → Этот файл определяет формат
2. СКИЛЛ    → .claude/skills/{формат}/SKILL.md + модули
3. БРЕНД    → brand/ (голос, аудитория, экспертиза)
4. МОДУЛЬ   → modules/{формат}/CLAUDE.md (настройки проекта)
5. ОБУЧЕНИЕ → learning/ (паттерны, анти-паттерны)
```

### Agents

| Агент | Роль |
|-------|------|
| AI Operator | Управление, решения |
| Threads Writer | Посты для Threads |
| YouTube Producer | Сценарии для YouTube |
| Critics (3) | Sales, Creative, Structure |
| Analyst | Анализ метрик |

### Принципы

1. **Lazy loading** — загружаются только нужные модули (~70% экономия токенов)
2. **No duplication** — проекты наследуют от skills, не копируют
3. **Learning loop** — система учится из твоих правок

---

## Поддержка

- Telegram: [@maximgalson](https://t.me/maximgalson)
- Канал: [@galsonproai](https://t.me/galsonproai)

---

*Фабрика Контента v2.0*  
*Макс Галсон • [galson.pro](https://galson.pro)*
