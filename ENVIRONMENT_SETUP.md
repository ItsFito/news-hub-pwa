# ⚙️ Environment Setup Guide

Panduan untuk setup environment development untuk News Hub PWA.

## 🖥️ Sistem Requirements

### Minimum

- **OS**: Windows 7+ / Mac / Linux
- **RAM**: 2GB
- **Storage**: 500MB (untuk dependencies)
- **Browser**: Chrome 40+ / Firefox 44+ / Safari 11+ / Edge

### Recommended

- **OS**: Windows 10/11 / macOS 10.15+ / Ubuntu 18.04+
- **RAM**: 4GB+
- **Storage**: 5GB (for development)
- **Browser**: Chrome/Edge latest

---

## 📦 Prerequisites Installation

### 1. Python (Required for local testing)

#### Check if Python installed

```bash
python --version
```

#### If not installed:

1. Go to: https://www.python.org/downloads/
2. Download Python 3.9+
3. Run installer
4. **Important**: Check "Add Python to PATH"
5. Click Install

#### Verify installation

```bash
python --version
python -m http.server --help
```

### 2. Git (Optional but recommended)

#### Check if Git installed

```bash
git --version
```

#### If not installed:

1. Go to: https://git-scm.com/download/
2. Download for your OS
3. Run installer
4. Use default settings
5. Finish installation

#### Verify installation

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### 3. Node.js (Optional, for better tooling)

#### Check if Node installed

```bash
node --version
npm --version
```

#### If not installed:

1. Go to: https://nodejs.org/
2. Download LTS version
3. Run installer
4. Use default settings
5. Finish installation

#### Verify installation

```bash
node --version
npm --version
npm install -g http-server  # Optional tool
```

---

## 📁 Project Setup

### 1. Clone atau Download Project

#### Option A: Via Git (Recommended)

```bash
git clone https://github.com/username/news-hub-pwa.git
cd news-hub-pwa
```

#### Option B: Download ZIP

1. Go to GitHub repository
2. Click "Code" → "Download ZIP"
3. Extract file
4. Navigate ke folder

#### Option C: Already have files

```bash
# Just navigate to the folder
cd c:\Users\Azzam\source\Modul 3
```

### 2. Verify File Structure

```bash
# Check all files exist
dir
# or on Mac/Linux
ls -la

# Should show:
# - index.html
# - styles.css
# - sw.js
# - manifest.json
# - package.json
# - README.md
# - ... (and more docs)
```

---

## 🚀 Development Environment

### Text Editor Setup

#### VS Code (Recommended)

1. Download: https://code.visualstudio.com/
2. Install
3. Open project folder in VS Code
4. Install extensions:
   - "Live Server" (ritwickdey.liveserver)
   - "HTML, CSS, JS Snippets" (ecmel.vscode-html-css)
   - "Markdown All in One" (yzhang.markdown-all-in-one)

#### Sublime Text

1. Download: https://www.sublimetext.com/
2. Install
3. Open folder: File → Open Folder

#### Notepad++

1. Download: https://notepad-plus-plus.org/
2. Install
3. Open project folder

### Browser Developer Tools Setup

#### Chrome/Edge

1. Press `F12` atau `Ctrl+Shift+I`
2. Enable features untuk PWA testing:
   - Application tab
   - Console tab
   - Network tab

#### Firefox

1. Press `F12` atau `Ctrl+Shift+I`
2. Enable features:
   - Storage tab
   - Console tab
   - Network tab

---

## 🔧 Local Server Setup

### Method 1: Python HTTP Server (Easiest)

```bash
# Navigate to project
cd c:\Users\Azzam\source\Modul 3

# Run server
python -m http.server 8000

# Output:
# Serving HTTP on 0.0.0.0 port 8000
# Open browser: http://localhost:8000
```

### Method 2: Python SimpleHTTPServer (Python 2)

```bash
# For Python 2 users
python -m SimpleHTTPServer 8000
```

### Method 3: Node.js HTTP Server

```bash
# Install (one time)
npm install -g http-server

# Run server
cd c:\Users\Azzam\source\Modul 3
http-server -p 8000

# Visit: http://localhost:8000
```

### Method 4: VS Code Live Server

1. Install extension "Live Server"
2. Right-click index.html
3. Select "Open with Live Server"
4. Auto-opens browser on http://127.0.0.1:5500

---

## 🧪 Testing Tools Setup

### Browser DevTools

- **Purpose**: Debug, test PWA features
- **How**: Press F12
- **Key tabs**: Application, Console, Network

### Lighthouse (Chrome Built-in)

- **Purpose**: PWA quality audit
- **How**: F12 → Lighthouse tab → Generate report
- **What to check**: Performance, PWA, Accessibility

### Testing Checklist

See: `TESTING.md` in project folder

---

## 🌐 Vercel Setup (For Deployment)

### 1. Create Vercel Account

1. Go to: https://vercel.com/signup
2. Sign up with GitHub / Email
3. Create account

### 2. Create GitHub Repository

1. Go to: https://github.com/new
2. Create repository: `news-hub-pwa`
3. Clone to local:
   ```bash
   git clone https://github.com/username/news-hub-pwa.git
   cd news-hub-pwa
   ```

### 3. Connect GitHub to Vercel

1. Go to Vercel Dashboard
2. Settings → GitHub
3. Connect GitHub account
4. Grant permissions

### 4. Import Project to Vercel

1. Dashboard → Add New → Project
2. Select repository
3. Click Import
4. Configure & Deploy

See: `DEPLOYMENT.md` for detailed steps

---

## 🔐 Security Setup (Optional)

### Git Configuration

```bash
# Configure git user
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Setup SSH key (optional)
# See: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
```

### Environment Variables

For this project, tidak perlu (semua static).
Namun untuk future projects:

```bash
# Create .env file
cp .env.example .env

# Add secrets (gitignored)
```

---

## 📊 Development Workflow

### Daily Workflow

```bash
# 1. Navigate to project
cd c:\Users\Azzam\source\Modul 3

# 2. Start server
python -m http.server 8000

# 3. Open browser
# http://localhost:8000

# 4. Open text editor
# code .  (VS Code)

# 5. Make changes
# Edit HTML, CSS, JS files

# 6. Refresh browser
# Ctrl+R or F5

# 7. Test changes
# Check all pages work

# 8. When done, stop server
# Ctrl+C in terminal
```

### Version Control Workflow

```bash
# 1. Check status
git status

# 2. Add changes
git add .

# 3. Commit
git commit -m "Description of changes"

# 4. Push to GitHub
git push origin main

# 5. Vercel auto-deploys!
```

---

## 🧠 Project Structure Quick Reference

```
news-hub-pwa/
│
├── 📄 Core Files
│   ├── index.html          ← Main app
│   ├── styles.css          ← Styling
│   ├── sw.js              ← Service Worker
│   └── manifest.json      ← PWA config
│
├── 📋 Config Files
│   ├── package.json        ← NPM config
│   ├── vercel.json        ← Vercel config
│   ├── .gitignore         ← Git ignore
│   └── robots.txt         ← SEO config
│
├── 📖 Documentation
│   ├── README.md                  ← Full docs
│   ├── QUICK_START.md            ← 5 min guide
│   ├── TESTING.md                ← Test guide
│   ├── DEPLOYMENT.md             ← Deploy guide
│   ├── UPDATE_PROFILE.md         ← Profile guide
│   ├── PROJECT_SUMMARY.md        ← Summary
│   ├── DOCUMENTATION_INDEX.md    ← Docs index
│   └── ENVIRONMENT_SETUP.md      ← This file
│
└── 📁 Optional Folders (create as needed)
    ├── .git                ← Git repository
    └── node_modules/       ← NPM packages
```

---

## ✅ Setup Verification Checklist

Run this to verify everything is setup correctly:

### Python Check

```bash
python --version
# Should return: Python 3.x.x

python -m http.server --help
# Should show help text
```

### Git Check

```bash
git --version
# Should return: git version 2.x.x
```

### Project Files Check

```bash
cd c:\Users\Azzam\source\Modul 3
dir  # Windows
ls   # Mac/Linux

# Should show all 16 files
```

### Browser DevTools Check

1. Open http://localhost:8000 (if server running)
2. Press F12
3. Go to Application tab
4. Check Service Worker status
5. Check Manifest loaded

### Lighthouse Check

1. Open DevTools (F12)
2. Go to Lighthouse
3. Click "Generate Report"
4. Should complete without critical errors

---

## 🐛 Troubleshooting Setup

### "Python not found"

**Solution**:

1. Download Python from python.org
2. Install with "Add to PATH" checked
3. Restart terminal/CMD
4. Verify: `python --version`

### "Port 8000 already in use"

**Solution**:

```bash
# Use different port
python -m http.server 9000
# Visit: http://localhost:9000
```

### "Service Worker not registering"

**Solution**:

1. DevTools → Application → Clear site data
2. Close all tabs of localhost
3. Hard refresh: Ctrl+Shift+R
4. Reload

### "Git command not found"

**Solution**:

1. Download Git from git-scm.com
2. Install with default settings
3. Restart terminal
4. Verify: `git --version`

### "DevTools Application tab empty"

**Solution**:

1. Use HTTPS or localhost
2. http://localhost:8000 should work
3. Check browser console for errors
4. Try different browser

---

## 📚 Next Steps

After setup:

1. ✅ Follow **QUICK_START.md**
2. ✅ Follow **TESTING.md**
3. ✅ Follow **DEPLOYMENT.md**

---

## 🎯 Summary

**Minimum Setup (5 minutes)**:

- [ ] Python installed
- [ ] Project files ready
- [ ] Run `python -m http.server 8000`
- [ ] Visit `http://localhost:8000`

**Recommended Setup (15 minutes)**:

- [ ] Python installed
- [ ] Git installed
- [ ] VS Code or text editor ready
- [ ] Browser DevTools familiar
- [ ] Local server running
- [ ] DevTools tested

**Full Setup (30 minutes)**:

- [ ] Python installed
- [ ] Git installed & configured
- [ ] VS Code with extensions
- [ ] Node.js installed
- [ ] Vercel account created
- [ ] GitHub account ready
- [ ] Local testing complete

---

**Ready to code? Start with QUICK_START.md! 🚀**
