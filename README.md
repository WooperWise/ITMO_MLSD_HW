# ITMO MLSD — домашние задания

Репозиторий домашних заданий курса **ITMO ML System Design** ([справочные материалы курса](https://mlops.ml-devs.com/)).

Каждая домашняя работа — ветка `hw_n` и PR в `main`: ревью ментора и двух кросс-ревьюверов, мерж только после ревью.

## ДЗ1 — сетап репозитория и ML-дизайн-док

- Условие: [itmo_mlsd_hw_1.md](itmo_mlsd_hw_1.md)
- Результат: [docs/ml_system_design_doc.md](docs/ml_system_design_doc.md) — дизайн-документ по шаблону [Reliable ML](https://github.com/IrinaGoloshchapova/ml_system_design_doc_ru) для проекта **absorbix-ai**
- Сетап: ruff (линтер + форматер) в [pyproject.toml](pyproject.toml), pre-commit в [.pre-commit-config.yaml](.pre-commit-config.yaml)

## О проекте absorbix-ai

**absorbix-ai** — ИИ-платформа поддержки предэкспериментальных решений по оптимизации всасывания и лекарственной формы препаратов: профиль вещества, диагностика ограничивающего фактора (растворимость, проницаемость, стабильность, метаболизм первого прохождения), подбор стратегий с проверяемыми источниками и уровнями доказательности.

> Исследовательский прототип. Не медицинский советчик: платформа не предназначена для назначения лечения, смены препаратов или подтверждения безопасности рецептур.

Код проекта: [absorbix-ai](https://github.com/WooperWise/absorbix-ai)

## Инструменты

```bash
uv sync                        # окружение (Python 3.12)
uv run pre-commit install      # включить pre-commit hooks
uv run pre-commit run --all-files
uv run ruff check .            # линтер
uv run ruff format --check .   # форматер
```
