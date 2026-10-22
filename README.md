# Flet Chat App

একটি Flet (Python) chat app। User প্রথমে নিজের তথ্য দেয়, তারপর একটি fake search দেখানো হয়, এরপর AWS backend-এর সাথে chat শুরু হয়।

## Flow

1. **Profile form:** Name, Location, Age, Education, Looking for
2. **Searching screen:** কয়েক সেকেন্ডের fake search animation
3. **Chat screen:** Online status সহ chat, প্রতিটি message-এর সাথে profile API-তে যায়

## Project structure

```
flet-chat-app/
├── main.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Local-এ চালানো

```bash
pip install -r requirements.txt
flet run main.py
```

## API

- Endpoint: `POST https://tbpc3gdax9.execute-api.eu-north-1.amazonaws.com/chat`
- Request body:

```json
{
  "message": "Hello",
  "user": {
    "name": "...",
    "location": "...",
    "age": "...",
    "education": "...",
    "interest": "..."
  }
}
```

- Response থেকে `reply` অথবা `message` key পড়া হয়।

## GitHub-এ push করা

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<username>/flet-chat-app.git
git push -u origin main
```

## Android APK build

```bash
flet build apk
```
