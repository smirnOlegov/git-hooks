# git-hooks
# Git Hooks 

Автоматизация проверки кода с помощью Git Hooks.

## 🔹 Что реализовано
- **pre-commit hook**:
  - блокирует коммит, если в коде есть `TODO`;
  - блокирует коммит, если в коде есть отладочный `print()`;
  - проверяет стиль кода с помощью [black](https://black.readthedocs.io/) (PEP8 autoformatter).

## 🧪 Тесты
1. Попытка закоммитить файл с `TODO` → ❌ коммит не проходит.  
2. Попытка закоммитить файл с `print()` → ❌ коммит не проходит.  
3. Коммит без ошибок → ✅ проходит успешно.  

## 🔧 Установка
1. Склонируйте репозиторий:
   ```bash
   git clone https://github.com/smirnOlegov/git-hooks-sample.git
   cd git-hooks-sample

2. Скопируйте хуки:
     ```bash
     git config core.hooksPath .githooks
     chmod +x .githooks/*

3. Установите black (если не установлен):
     ```bash
     pip install black
