# Что нового — Конструктор Фабрики Контента

История обновлений. После `git pull` или скачивания новой версии — смотри что появилось.

---

## [1.14] — 2026-02-09

### Новые скиллы
- **Veo Video** — полный пайплайн генерации видео через Veo 3.1 (text-to-video, image-to-video, timelapse, reference images, video extension). Включает prompting guide, best practices, async API, prompt library
- **Timelapse Creator** — специализированный скилл для создания таймлапсов: идея → keyframes → согласование → видео → доставка
- **SEO Blog Writer** — автономное написание SEO-статей со скриншотами через microlink.io, верификацией и готовыми к публикации

### Расширения
- **Customer Research** — добавлены 3 новых файла:
  - `anarbaeva-custdev.md` (20KB) — методология кастдева по Анарбаевой: 6 блоков вопросов, температуры аудитории, техника "голосование рублём"
  - `segment-selection.md` — выбор сегмента и матрица гипотез
  - `ai-automation.md` — автоматизация кастдевов через ИИ
- **Offer Core** — добавлен `anarbaeva-products.md` (8KB) — продуктовая матрица и ценообразование по Анарбаевой

### Системные
- **UFC (Unified Field Context)** — система автоподтягивания релевантного контекста при генерации контента (voice-style + learning)
- **Brain Structure** — шаблон для стратегии и накопления знаний:
  - `goals/` — weekly, monthly, yearly цели
  - `research/` — audience-insights, competitors, market-trends
  - `architecture/` — tools-stack, automations, integrations

### Структура
```
Новые файлы:
├── .claude/skills/veo-video/           # +13KB
├── .claude/skills/timelapse-creator/   # +5KB
├── .claude/skills/seo-blog-writer/     # +5.5KB
├── agents/products/customer-research/  # +36KB
├── agents/products/anarbaeva-products.md # +8KB
├── tools/ufc/                          # +2KB
└── brain/                              # +4KB шаблонов
```

---

## [1.13] — 2026-02-07

### Новое
- **Продающие паттерны Тимочко** — 1200+ строк (63KB) паттернов продающей психологии
- **Паттерны запусков Тимочко** — 50KB паттернов запуска продуктов (PLF + lifestyle)
- **Позиционирование по Анарбаевой** — 34KB фреймворк позиционирования
- **Формулы Сердитова** — экспресс-запуски и монетизация
- **Tripwire skill** — создание tripwire-продуктов
- **Product Types** — типология продуктов для запуска
- **Воронки по Анарбаевой** — структуры воронок для запусков
- **Shared Learnings** — универсальные approved/anti-patterns, SOURCES, TONE-FORMULAS

### Обновлено
- `selling-meanings/psychology.md` — +48% контента
- `selling-meanings/templates.md` — +56% контента
- `selling-meanings/SKILL.md` — обновлённый роутер
- `launch/SKILL.md` — расширенные триггеры и интеграции

---

## [1.12] — 2026-02-07

### Новое
- **Reels skill** — полная переработка (x3 контента): методология, ВИСП-формулы, 12+ структур, адаптация для HeyGen
- **Storytelling** — 2 новых файла: "Блог как сериал" + "Прогрев = история"
- **TikTok project example** — шаблон для медицинских экспертов
- **Anarbaeva Reels** — методология форматов контента

### Обновлено
- `reels/SKILL.md` — x1.7 обновление
- `reels-methodology.md` — x3 контента (439 → 1375 строк)
- `psychological-triggers.md` — расширены триггеры и примеры

---

## [1.11] — 2026-02-05

### Новое
- **3 агента для продуктов:** offer-core, meaning-unpacking, customer-research
- **Constructor-improvement skill** — улучшение конструктора изнутри
- **Документация v2** — полностью переработаны все docs/

### Обновлено
- Critics (sales-critic, creative-critic, structure-critic)
- QUICK-START.md, INSTALL.md, UPDATE-GUIDE.md
- README.md — актуализирован
- agents/_index.md — обновлён роутинг

---

## [1.10] — 2026-02-04

### Новое
- **Copywriting skill** — Халилов + Шугерман (slippery slide)
- **Editing skill** — правила Ильяхова + persuasion
- **Headlines skill** — attention patterns + формулы заголовков
- **Reels structures** — 7 структур сценариев

### Обновлено
- `storytelling/hooks.md` — расширены хуки
- `storytelling/formulas.md` — новые формулы

---

## [1.09] — 2026-02-01

### Новое
- **Nano Banana Web skill** — генерация через веб-интерфейс
- **RESOURCES.md** — обновлённый список ресурсов

---

## [1.08] — 2026-01-26

### Hotfix (2026-01-26)
- Удалён Blog Chronicler (личный инструмент)
- Добавлен Advanced Skills Showcase

### Новое
- **Transcription Processor** — обработка видео-транскрибаций
- **Telegram Skill** — методология Telegram-постов (адаптация VISP)
- **Agent Architect Skill** — создание production-ready агентов

### Улучшено
- **Learning Agent v1.0** — глобальное обучение
- Обновлены AGENTS-ROUTING.md и SKILLS-ROUTING.md

---

## [1.06] — 2026-01-20

### Новое
- **Триггеры для агентов** — простые слова активируют агентов
- Документация по триггерам и командам

### Улучшено
- Analyst Agent v1.1 — автоактивация
- Selling Meanings Agent v1.2 — автоактивация

---

## [1.05] — 2026-01-19

### Новое
- **Формат "Мой стек"** — структура постов про инструменты
- Правила нумерованных списков vs тире

---

## [1.04] — 2026-01-19

### Новое
- **Автообучение стилю** — система запоминает удачные посты
- Команды: `это сработало`, `это не сработало`, `запомни пример`
- **HeyGen skill** — генерация видео с AI-аватарами
- **Nano Banana** — промпты для обложек

---

## [1.03] — 2026-01-19

### Новое
- Защита данных при обновлении через git

---

## [1.02] — 2026-01-18

### Новое
- Советы как не звучать как нейросеть
- Техника выноса CTA в отдельный пост

---

## [1.01] — 2026-01-17

### Новое
- `интервью мини` — быстрое интервью за 10 минут
- Quick Start: "Первый пост за 30 минут"

---

## [1.00] — 2026-01-10

### Новое
- Первая версия конструктора
- 11 навыков: youtube, threads, reels, carousel, nano-banana и другие
- Шаблон проекта с интервью

---

## Как обновляться

См. [UPDATE-GUIDE.md](UPDATE-GUIDE.md)

---

## Поддержка

Сайт: [galson.pro](https://galson.pro) | Вопросы: [@maximgalson](https://t.me/maximgalson) | Канал: [@galsonproai](https://t.me/galsonproai)

---

*Фабрика Контента v1.14*  
*Макс Галсон • [galson.pro](https://galson.pro)*
