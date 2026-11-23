# AgentHub B2B — Android APK (Capacitor + GitHub Actions)

## Como subir via Termux e compilar no GitHub

1. Extraia este pacote no armazenamento do seu Android (ex: `/sdcard/Download/agenthub_android`).
2. Abra o **Termux** e execute:

```bash
termux-setup-storage
mkdir -p ~/agenthub-b2b
cp -r /sdcard/Download/agenthub_android/. ~/agenthub-b2b/
cd ~/agenthub-b2b

git init
git branch -M main
git add .
git commit -m "Versao inicial AgentHub B2B Android"
git remote add origin https://github.com/dieimesjost-sys/agenthub-b2b.git
git push -u origin main
```

3. No GitHub, acesse a aba **Actions** do repositório `agenthub-b2b`, aguarde o workflow **Build Android APK** finalizar e baixe o arquivo `AgentHub-B2B-v1.0-debug`.
