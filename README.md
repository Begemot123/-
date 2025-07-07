git clone https://github.com/Begemot123/-.git
cd -
backend:
  name: git-gateway
  branch: main

media_folder: "static/uploads"
public_folder: "/uploads"

collections:
  - name: "news"
    label: "Новости"
    folder: "content/news"
    create: true
    fields:
      - { label: "Заголовок", name: "title", widget: "string" }
      - { label: "Текст", name: "body", widget: "markdown" }
  - name: "team"
    label: "Команда"
    folder: "content/team"
    create: true
    fields:
      - { label: "Имя", name: "name", widget: "string" }
      - { label: "Описание", name: "description", widget: "text" }
      - { label: "Фото", name: "image", widget: "image" }
  - name: "schedule"
    label: "Расписание"
    folder: "content/schedule"
    create: true
    fields:
      - { label: "Дата", name: "date", widget: "datetime" }
      - { label: "Событие", name: "event", widget: "string" }
git add .
git commit -m "Добавлен сайт Фемитошек"
git push origin main
