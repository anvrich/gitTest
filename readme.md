# 📜 Шпаргалка по Git:

<details> 
<summary>🖱️2.9 Удаление и Переименование файлов</summary>

## 🚮 Удаление файлов (`git rm`)

<details>
<summary>🖱️ Раскрыть команды и примеры</summary>

Команда `git rm` удаляет файлы из рабочей директории и индекса (staging area), подготавливая их к коммиту.

### Основные варианты:

- **`git rm <файл>`**  
  Удаляет файл из рабочей директории и индекса.  
  _Пример_:
  ```bash
  git rm oldfile.txt
  git commit -m "Удалил oldfile.txt"
  ```

- **`git rm -f <файл>`**  
  Принудительно удаляет файл, даже если есть несохранённые изменения.  
  _Пример_:
  ```bash
  git rm -f draft.txt  # Удалит, игнорируя изменения
  ```

- **`git rm -r <директория>`**  
  Рекурсивно удаляет директорию и все её содержимое.  
  _Пример_:
  ```bash
  git rm -r old_folder/
  git commit -m "Удалил папку old_folder"
  ```

- **`git rm --cached <файл>`**  
  Удаляет файл только из индекса, оставляя его в рабочей директории. Полезно, чтобы перестать отслеживать файл.  
  _Пример_:
  ```bash
  git rm --cached log.txt
  git commit -m "Перестал отслеживать log.txt"
  ```

</details>

---

## 🔄 Переименование файлов (`git mv`)

<details>
<summary>🖱️ Раскрыть команды и примеры</summary>

Команда `git mv` переименовывает или перемещает файлы, автоматически обновляя индекс.

### Основные варианты:

- **`git mv <старое_имя> <новое_имя>`**  
  Переименовывает файл и добавляет изменение в индекс.  
  _Пример_:
  ```bash
  git mv file1.txt file2.txt
  git commit -m "Переименовал file1.txt в file2.txt"
  ```

- **Ручной способ**:  
  Если хочешь переименовать без `git mv`:
  ```bash
  mv file1.txt file2.txt
  git add file2.txt
  git rm --cached file1.txt
  git commit -m "Переименовал file1.txt в file2.txt"
  ```

</details>
</details>


<details>
<summary>🖱️ 3.1  Ветки – Введение </summary>

####   

<details>
<summary>🌿 3.2 Git – Ветки – Создание и переключение</summary>

- **`git branch`** – список веток
- **`git branch -v`** – список веток с коммитами
- **`git branch <имя>`** – создать ветку (например, `feature`)
- **`git checkout <имя>`** – переключиться на ветку
- **`git checkout -b <имя>`** – создать и переключиться

</details>

####   
<details>
<summary>🌿 3.3 Git – Ветки – Команда checkout при незакоммиченных изменениях</summary>

- **`git checkout -f master`** – принудительно на master, отбрасывает изменения
- **`git checkout -f HEAD`** – сбрасывает до HEAD, убирает изменения
- **`git checkout -f`** – то же, что и -f HEAD, для текущей ветки
- **`git stash`** – прячет изменения в "тайник"
- **`git checkout <обратно>`** – переключается обратно на ветку
- **`git stash pop`** – возвращает спрятанные изменения

</details>

</details>
