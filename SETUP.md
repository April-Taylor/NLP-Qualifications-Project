# 🔧 Google Colab + GitHub + Drive Integration Setup

This guide explains how to use the `Colab Git Setup` notebook to initialize and manage your project environment across Google Colab, Google Drive, and GitHub.

## 📌 What This Setup Does

- Mounts Google Drive and creates a working project directory.
- Clones a GitHub repository into your Drive (if not already present).
- Configures Git with your identity.
- Loads API tokens securely from Colab's Secrets tool.
- Generates common project folders (`notebooks/`, `models/`, `src/`, etc.).
- Creates a `README.md` if missing.
- Performs an initial Git push.
- Allows Git pushes at the end of every session.

## 🧭 How to Use This Notebook

### 1️⃣ To **initiate a new project**:
- Update the `USER INPUT` section with your GitHub username, repo name, and email.
- Run the notebook from top to bottom (includes the first Git push).

### 2️⃣ To **start a new session**:
- Run the notebook from top through the `RUN SETUP` section to remount Drive and reload secrets.

### 3️⃣ To **end a session**:
- Run the final `END-OF-SESSION PUSH` section to commit and push any changes to GitHub.

## 🔐 Required Colab Secrets

Go to **Colab > Settings > Secrets** and add the following:

- `GitHubToken` – your GitHub Personal Access Token
- `wandb` – (optional) Weights & Biases key
- `UMLS` – (optional) UMLS API key

## 🧪 Recommended Folder Structure

The setup will auto-create:

```
notebooks/
models/
data/
src/
outputs/
```

Each includes a `.gitkeep` file so they persist in GitHub.

---

Maintained by **April Taylor**, 2025