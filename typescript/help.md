[Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

## TypeScript

1. Встановити TypeScript __локально__

Встановити зі стандартними параментрами, по замовчуванню (пізніше можна змінити у файлі json) 

> npm init -y


або, встановити вручну (з налаштуваннями)

> npm install  


2. Перетворити файл TypeScript на файл JS

> npx tsc <імя файла>.ts


Команда `npx` оначає що ми беремо локальний пекет (якщо його нема то тоді глобальний)

Якщо команда відпрацювала, має зявитися файл js


3. Файл __Tsconfig.json__ вказує на те що поточна директорія є коренем проекту, і при запуску 
будуть будуть виконуватися налаштування з цього файла


- sourceMap - створити карту для пошуку (для виправлення помилок, на час розробки)

- outDir - папка для виведення файлів 

- include - звідки брати файли

- exclude - не 'компілювати' файли з цієї папки 

        {
            "compilerOptions": {
                "module": "CommonJS",
                "noImplicitAny": true,
                "removeComments": true,
                "sourceMap": true,
                "outDir": "./dist"
            },
            "include": ["./src/**/*"],
            "exclude": ["node_modules"]
        }