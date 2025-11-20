# goit-node-cli

Домашнє завдання. Тема 2. Створення консольних додатків

## Опис проєкту

Консольний додаток для управління контактами. Дозволяє виконувати основні CRUD операції (створення, читання, оновлення, видалення) з контактами через командний рядок.

## Встановлення

1. Клонуйте репозиторій:
```bash
git clone https://github.com/Serhii-Palamarchuk/goit-node-cli.git
cd goit-node-cli
```

2. Встановіть залежності:
```bash
npm install
```

## Використання

Додаток підтримує наступні команди:

### Отримати список всіх контактів

```bash
node index.js -a list
```

Виводить всі контакти у вигляді таблиці.

### Отримати контакт за ID

```bash
node index.js -a get -i <contactId>
```

**Приклад:**
```bash
node index.js -a get -i 05olLMgyVQdWRwgKfg5J6
```

Виводить об'єкт контакту з вказаним ID або `null`, якщо контакт не знайдено.

### Додати новий контакт

```bash
node index.js -a add -n <name> -e <email> -p <phone>
```

**Приклад:**
```bash
node index.js -a add -n Mango -e mango@gmail.com -p 322-22-22
```

Додає новий контакт і виводить об'єкт створеного контакту з унікальним ID.

### Видалити контакт

```bash
node index.js -a remove -i <contactId>
```

**Приклад:**
```bash
node index.js -a remove -i qdggE76Jtbfd9eWJHrssH
```

Видаляє контакт з вказаним ID і виводить об'єкт видаленого контакту або `null`, якщо контакт не знайдено.

## Параметри командного рядка

- `-a, --action <type>` - тип дії (list, get, add, remove)
- `-i, --id <type>` - ID контакту (для get та remove)
- `-n, --name <type>` - ім'я контакту (для add)
- `-e, --email <type>` - email контакту (для add)
- `-p, --phone <type>` - телефон контакту (для add)

## Структура проєкту

```
goit-node-cli/
├── db/
│   └── contacts.json    # База даних контактів
├── contacts.js          # Модуль для роботи з контактами
├── index.js            # Головний файл додатку
├── package.json        # Залежності та налаштування проєкту
└── README.md          # Документація
```

## Технології

- Node.js
- Commander.js - парсинг аргументів командного рядка
- nanoid - генерація унікальних ID
- fs/promises - робота з файловою системою

## Автор

Serhii Palamarchuk
