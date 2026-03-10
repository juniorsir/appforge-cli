# ▲ AppForge CLI

**The Universal App Builder**

Convert your **web, Flutter, or native Android projects** into installable mobile apps with a single command, powered by **free GitHub cloud builds**.

AppForge is a command-line tool designed for developers who want a **fast, automated way to create Android (`.apk`) and iOS (`.zip` Xcode projects)** builds without complex local setups.

---

# ✨ Features

### Universal Framework Support
Build apps from multiple frameworks including:

- React
- Vite
- Next.js
- Flutter
- Native Android (Kotlin / Java)
- And more

---

### Zero Configuration
AppForge **automatically detects your project type** and sets up the complete build pipeline.

No manual configuration required.

---

### Cloud-Powered Builds
AppForge uses **free GitHub Actions runners** to compile your apps.

That means:

- ❌ No Android Studio required  
- ❌ No Xcode required  
- ❌ No heavy local setup  

---

### AI-Powered Permissions
AppForge scans your web code to detect required native features like:

- Camera
- GPS
- Microphone
- File access

It then **automatically configures the necessary permissions**.

---

### Vercel-like CLI Experience
A clean and modern interactive terminal experience.

You get:

- guided prompts
- real-time status
- beautiful CLI output

---

### Cross-Platform
Generate builds from **any operating system**.

| OS | Supported |
|----|-----------|
| Windows | ✔ |
| macOS | ✔ |
| Linux | ✔ |
| Termux | ✔ |

---

# ⚙️ How It Works

AppForge uses a **two-repository architecture**.

## 1️⃣ appforge-cli (Local Tool)

Installed on your machine.

Responsibilities:

- Detect project type
- Configure build
- Package project
- Upload to cloud

---

## 2️⃣ appforge-build (Cloud Builder)

A repository you fork.

Responsibilities:

- Run GitHub Actions
- Compile the app
- Produce `.apk` or `.zip`

---

### Why this architecture?

Because:

- You use **your own GitHub free build minutes**
- No external servers needed
- Full control of builds

---

# 🚀 Getting Started in 60 Seconds

## Step 1 — Fork the Cloud Builder

Go to the **AppForge Build Template** repository and click:

```
Fork
```

This creates your **personal build server**.

You only need to do this **once**.

---

# Step 2 — Install AppForge CLI

Open your terminal and install globally.

```bash
pip install appforge-cli
```

Then verify:

```bash
appforge --help
```

---

# Step 3 — Create a GitHub Token

AppForge needs permission to upload code to your build repository.

Go to:

```
https://github.com/settings/tokens
```

Create a **Fine-grained token**.

Settings:

**Name**

```
AppForge CLI Token
```

---

### Repository Access

Select:

```
Only select repositories
```

Choose your forked:

```
appforge-build
```

---

### Permissions

Grant:

```
Actions → Read and write
Contents → Read and write
```

Generate the token and **copy it**.

---

# Step 4 — Build Your First App

Navigate to your project folder.

```bash
cd my-awesome-react-app
```

Initialize AppForge.

```bash
appforge init
```

AppForge will:

- detect framework
- configure build settings
- create project config

---

Start your first cloud build.

```bash
appforge build
```

Paste your **GitHub token** when asked.

---

### Check build status

```bash
appforge status
```

---

### Download your app

```bash
appforge download
```

Your compiled app will appear locally.

---

# 📦 Supported Project Types

| Framework | Detection | Notes |
|-----------|-----------|------|
| Flutter | `pubspec.yaml` | Uses Flutter SDK |
| Native Android | `build.gradle` | Builds with Gradle |
| React (CRA) | `react-scripts` | Wrapped with Capacitor |
| Vite | `vite.config.js` | Wraps `dist` folder |
| Next.js | `next.config.js` | Requires `output: 'export'` |
| Angular | `@angular/core` | Wraps `dist` |
| SvelteKit | `@sveltejs/kit` | Requires static adapter |
| Nuxt.js | `nuxt.config.js` | Requires `nuxt generate` |
| Plain HTML | `index.html` | Packaged into `www` |

---

# 🧠 Example Workflow

```
cd my-project

appforge init
appforge build
appforge status
appforge download
```

Done. Your app is ready.

---

# 🤝 Contributing

Contributions are welcome!

You can help by:

- Reporting bugs
- Suggesting features
- Submitting pull requests

Start by opening an **Issue**.

---

# 📜 License

This project is licensed under the **MIT License**.

Feel free to use, modify, and distribute.

---

# ⭐ Support the Project

If you like AppForge, consider:

⭐ Starring the repository  
🔁 Sharing with developers  
🐛 Reporting bugs  

---

# ▲ AppForge

**Build Apps. Anywhere. Instantly.**
