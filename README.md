# C++ Search Server 🔍

Образовательный проект на C++17 – простой поисковый движок с поддержкой TF-IDF ранжирования и фильтрации.

---

## ⚙️ Возможности

- **Добавление документов**, включая статусы (`ACTUAL`, `IRRELEVANT`, `BANNED`, `REMOVED`) и оценки.
- **Поиск с использованием TF-IDF**, с поддержкой:
  - стоп-слов;
  - отрицательных слов (мины);
  - многопоточного и однопоточного исполнения.
- **Методы класса `SearchServer`:**
  - `GetDocumentCount()`, `MatchDocument()`, `GetWordFrequencies()`, `RemoveDocument()` (с/без многопоточности).
- **Дополнительно:**
  - `PrintDocument()`, `Paginate()`, `RemoveDuplicates()`, класс `LogDuration` для профилирования.

---

## 🧩 Структура

- `search-server/` — основной код
- `main.cpp`, `test_example_functions.h` — точка входа и тесты
- `CMakeLists.txt` — конфигурация сборки

---

## 🛠 Требования

- Компилятор: GCC или Clang с поддержкой C++17
- CMake
- ОС: Linux / macOS / Windows
- (Опционально) Python для утилиты `gil` — при использовании CI

---

## 🧱 Сборка

```bash
git clone https://github.com/aksi321/cpp-search-server.git
cd cpp-search-server

# Debug сборка
mkdir Debug && cd Debug
cmake -G "Unix Makefiles" ../ -DCMAKE_BUILD_TYPE=Debug
cmake --build .

# Или Release
cd .. && mkdir Release && cd Release
cmake -G "Unix Makefiles" ../ -DCMAKE_BUILD_TYPE=Release
cmake --build .
