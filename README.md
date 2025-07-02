# Chat Microservice App

This project is a chat microservice application running locally on Ubuntu 24.04 LTS and can be shared publicly via Ngrok tunnels.

---

## 📚 Prerequisites

- **Ubuntu 24.04 LTS**
- Apache/Nginx or Laravel Valet (or any HTTP server)
- Ngrok account (https://ngrok.com)

---

## 🚀 Local Development URL

Your app runs locally at:
http://chat-microservice-app.local
Make sure this domain is mapped in your `/etc/hosts`:


---

## 🌐 Exposing the App to Public Internet

We use **Ngrok** to share your local app securely.

### 1️⃣ Install Ngrok

```bash
sudo snap install ngrok
```

### 2️⃣ Connect Ngrok to your account
```bash
ngrok config add-authtoken {YOUR_NGROK_AUTHTOKEN}
```

### 3️⃣ Start Ngrok Tunnel
If your web server runs on port 80:

```bash
ngrok http --host-header=chat-microservice-app.local 80
```

This command forwards requests and preserves the host header.

You will get a forwarding URL like:

```bash
https://abc123.ngrok.io
```

Anyone with this URL can access your app.

### 💡 Notes

Update your .env:
```bash
APP_URL=https://abc123.ngrok.io
```

Remember to restart your app/server if needed.
Ngrok tunnels are temporary—restart Ngrok if your session expires.


