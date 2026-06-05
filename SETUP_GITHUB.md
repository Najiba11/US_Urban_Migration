# How to Push This to GitHub

Follow these steps to get this repository up on GitHub.

## Step 1 — Create a GitHub Account
If you don't have one already, sign up at [github.com](https://github.com/).

## Step 2 — Install Git
Download from [git-scm.com](https://git-scm.com/downloads). Verify it works:
```bash
git --version
```

## Step 3 — Create a New Repository on GitHub

1. Click the **"+"** icon in the top right → **"New repository"**
2. Name it: `us-urban-migration` (or whatever you prefer)
3. Add a short description: *"Analysis of US urban demographic change 2000-2020 using the GUDD dataset"*
4. Keep it **Public**
5. **DO NOT** check "Add README" or "Add License" (we already have these)
6. Click **"Create repository"**

## Step 4 — Push This Folder to GitHub

Open a terminal/command prompt and navigate to where you unzipped this repository:

```bash
cd path/to/us_migration_repo
```

Configure git (one-time setup):
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Initialize and push:
```bash
git init
git add .
git commit -m "Initial commit: US urban migration analysis"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/us-urban-migration.git
git push -u origin main
```

When prompted for password, use a **Personal Access Token** (PAT):
1. Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
2. Generate new token with `repo` scope
3. Use this token as your password

## Step 5 — Update Your README with the Real URL

Open `README.md` and replace all instances of `YOUR_USERNAME` with your actual GitHub username. Then:

```bash
git add README.md
git commit -m "Update repo URL in README"
git push
```

## Step 6 — (Optional) Add Topics and Description

On your GitHub repo page:
- Click the **gear icon** next to "About" on the right
- Add topics: `demography`, `urban-studies`, `data-visualization`, `migration`, `python`, `gudd`
- Add a website link if applicable

## Step 7 — Get the Data Locally

The data files are NOT in this repo (too large + not yours to redistribute). Download them from the original Zimmer et al. repository:

```bash
# Clone the original repo
git clone https://github.com/zimmermaps/urban_demography.git

# Copy needed files into your data folder
cp urban_demography/01_data/04_final_demographic_data/01_static_boundaries/*.zip data/
cp urban_demography/01_data/02_auxiliary_data/03_mapping.zip data/

# Unzip them
cd data
unzip "*.zip"
```

Or download from the **Harvard Dataverse** link in the original paper.

## Step 8 — Run the Analysis

```bash
python3.11 -m venv .venv
source .venv/bin/activate     # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/migration_pattern_analysis.ipynb` and run it!

---

## Common Issues

**"Permission denied" when pushing**
→ Use a Personal Access Token instead of password (Step 4)

**"Repository not found"**
→ Double-check the repo URL — replace `YOUR_USERNAME` with your actual GitHub username

**Large files rejected**
→ Make sure `.gitignore` is in place (it should be). Don't commit anything from `data/`.

**Want to update the repo later?**
```bash
git add .
git commit -m "Description of changes"
git push
```
