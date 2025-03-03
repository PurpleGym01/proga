# 1. Инициализация Git-репозитория (если ещё не инициализирован)
git init

# 2. Добавление всех файлов в репозиторий и первый коммит
git add .
git commit -m "Initial commit: CMake project setup"

# 3. Создание новой ветки featureutils
git branch featureutils
git checkout featureutils  # Переключаемся на новую ветку

# 4. Внесение изменений в utils.cpp (добавление функции умножения)
#    и обновление main.cpp для использования этой функции
# (редактируем файлы, затем добавляем и коммитим изменения)

git add utils.cpp main.cpp
git commit -m "feat: Add multiplication function to utils"

# 5. Переключение обратно на основную ветку (main или master)
git checkout main  # Если основная ветка называется master, замените main на master

# 6. Внесение изменений в main.cpp и коммит
git add main.cpp
git commit -m "fix: Update main output message in main branch"

# 7. Попытка слить ветку featureutils в основную
git merge featureutils

# 8. Разрешение конфликтов (если возникли)
# (открываем файлы, устраняем конфликты, затем продолжаем)

git add .
git commit -m "merge: Resolve conflicts between main and featureutils"

# 9. Отправка всех веток в удаленный репозиторий
git push --all origin
