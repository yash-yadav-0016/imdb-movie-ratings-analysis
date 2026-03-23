# 🚀 Quick Setup Guide - TMDB Movie Ratings Analysis

## Complete Step-by-Step Instructions

### ✅ Step 1: Prerequisites Check (2 minutes)

Before you start, ensure you have:

- [ ] **R installed** (version 4.0 or higher)
  - Download from: https://cran.r-project.org/
  - Check version: Open R console and type `R.version`

- [ ] **RStudio installed** (recommended)
  - Download from: https://www.rstudio.com/products/rstudio/download/

- [ ] **Internet connection** (for package downloads)

- [ ] **2+ GB free disk space**

- [ ] **Kaggle account** (for dataset download)

---

### ✅ Step 2: Download Dataset (5 minutes)

**Option A: Download from Kaggle**

1. Go to: https://www.kaggle.com/tmdb/tmdb-movie-metadata
2. Click "Download" button
3. This will download a ZIP file (~25 MB)
4. Extract the ZIP file to get:
   - `tmdb_5000_movies.csv`
   - `tmdb_5000_credits.csv`

**Option B: Use Kaggle CLI** (Advanced)

```bash
# Install Kaggle CLI
pip install kaggle

# Download dataset
kaggle datasets download -d tmdb/tmdb-movie-metadata

# Extract
unzip tmdb-movie-metadata.zip
```

---

### ✅ Step 3: Setup Project Folder (3 minutes)

**On Windows:**
```
1. Create new folder: C:\Users\yash0\Desktop\tmdb-analysis
2. Place the two CSV files there
3. Place the R script there
4. Your folder should look like:
   
   tmdb-analysis/
   ├── tmdb_analysis_complete.R
   ├── tmdb_5000_movies.csv
   ├── tmdb_5000_credits.csv
   └── README.md
```

**On Mac/Linux:**
```bash
# Create project directory
mkdir ~/tmdb-analysis
cd ~/tmdb-analysis

# Download and place files
# Download CSV files from Kaggle and move to this directory
cp ~/Downloads/tmdb_5000_*.csv ~/tmdb-analysis/

# Copy R script
cp tmdb_analysis_complete.R ~/tmdb-analysis/
```

---

### ✅ Step 4: Verify File Placement (1 minute)

**On Windows:**
- Open File Explorer
- Navigate to your project folder
- Should see 3 files:
  - `tmdb_5000_movies.csv` (size: ~5-10 MB)
  - `tmdb_5000_credits.csv` (size: ~10-15 MB)
  - `tmdb_analysis_complete.R` (size: ~50 KB)

**On Mac/Linux:**
```bash
# List files in project directory
ls -lh ~/tmdb-analysis/

# Should show:
# -rw-r--r--  8M tmdb_5000_movies.csv
# -rw-r--r-- 15M tmdb_5000_credits.csv
# -rw-r--r-- 50K tmdb_analysis_complete.R
```

---

### ✅ Step 5: Open in RStudio (1 minute)

1. **Open RStudio**
2. Go to: `File → Open File`
3. Navigate to your project folder
4. Select: `tmdb_analysis_complete.R`
5. Script will open in editor

---

### ✅ Step 6: Run the Analysis (10-20 minutes)

**Method 1: RStudio (Recommended)**
```
1. Click anywhere in the R script
2. Press: Ctrl + A (select all)
3. Press: Ctrl + Enter (run all)
4. Watch the console for progress
5. Analysis will complete in ~15-20 seconds
```

**Method 2: Run Entire Script**
```
1. Click in the R script window
2. Menu: Code → Run All
3. Or keyboard: Ctrl + Shift + S
```

**Method 3: Command Line**
```bash
# On Windows Command Prompt:
Rscript tmdb_analysis_complete.R

# On Mac/Linux Terminal:
Rscript tmdb_analysis_complete.R
```

---

### ✅ Step 7: Check Results (2 minutes)

After the script finishes, you should see in your project folder:

1. **tmdb_regression_analysis.png** (NEW)
   - 6-panel visualization dashboard
   - Open with any image viewer
   - Perfect for presentations/reports

2. **TMDB_ANALYSIS_REPORT.txt** (NEW)
   - Detailed analysis report
   - Open with any text editor
   - Copy-paste into Word/PowerPoint

3. **RStudio Console Output**
   - Shows all analysis steps
   - Displays key metrics
   - Look for: ✓ checkmarks for success

---

### ✅ Step 8: Push to GitHub (5 minutes)

**Create GitHub Repository:**

1. Go to: https://github.com/new
2. Enter Repository Name: `tmdb-ratings-analysis`
3. Description: "Complete data science project analyzing TMDB movie ratings"
4. Choose: Public (for portfolio) or Private
5. Click: "Create repository"

**Push Code to GitHub:**

```bash
# Navigate to your project folder
cd C:\Users\yash0\Desktop\tmdb-analysis  # Windows
# or
cd ~/tmdb-analysis  # Mac/Linux

# Initialize Git (one time)
git init
git add .
git commit -m "Initial commit: TMDB ratings analysis"

# Add GitHub remote (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/tmdb-ratings-analysis.git
git branch -M main
git push -u origin main
```

**After First Push:**
```bash
# For future updates
git add .
git commit -m "Description of changes"
git push
```

**OR Use GitHub Desktop (Easier):**

1. Download: https://desktop.github.com/
2. Create repository
3. Drag-drop files
4. Click "Publish repository"

---

### ⚠️ Troubleshooting

**Problem: "CSV file not found"**
- Solution: Ensure CSV files are in the same folder as R script
- Check file names match exactly (including .csv extension)

**Problem: "Package not found"**
- The script auto-installs packages
- If error persists, manually run:
  ```r
  install.packages(c("dplyr", "ggplot2", "corrplot", "jsonlite"))
  ```

**Problem: "Cannot find tmdb_5000_movies.csv"**
- Verify spelling exactly matches
- File size should be ~5-10 MB
- Make sure it's extracted from ZIP

**Problem: RStudio crashes**
- Close other applications
- Restart RStudio
- Try running from command line instead

**Problem: GitHub authentication fails**
- Use Personal Access Token instead of password
- Generate at: https://github.com/settings/tokens
- Use as password when pushing

---

### ✨ Success Indicators

You'll know everything worked when you see:

```
✓ Raw data loaded
✓ Data cleaned successfully  
✓ Features extracted from JSON
✓ Regression model created
✓ Cross-validation completed
✓ Visualization saved: tmdb_regression_analysis.png
✓ Results saved to: TMDB_ANALYSIS_REPORT.txt
✅ ANALYSIS COMPLETE!
```

---

### 📊 What to Submit to Professor

Recommended folder structure for submission:

```
tmdb-ratings-analysis/
├── README.md                          # Project description
├── tmdb_analysis_complete.R           # Main code
├── TMDB_ANALYSIS_REPORT.txt          # Generated report
├── tmdb_regression_analysis.png      # Generated visualization
└── .gitignore                         # GitHub setup
```

---

### 🎯 What to Include in GitHub

**DO Include:**
- ✓ R script
- ✓ README.md
- ✓ .gitignore
- ✓ Generated report (TMDB_ANALYSIS_REPORT.txt)
- ✓ Generated visualization (PNG)

**DON'T Include:**
- ✗ CSV files (too large, download from Kaggle)
- ✗ .Rhistory files
- ✗ .RData files
- ✗ Temporary files

---

### 📝 Sample GitHub Portfolio Description

Use this for your GitHub profile:

```
## TMDB Movie Ratings Analysis

Complete data science project analyzing what makes movies highly-rated 
using linear regression and exploratory data analysis.

**What I did:**
- Loaded and cleaned 5000+ movie records from TMDB dataset
- Engineered 7 new features from raw data
- Built multiple linear regression model
- Achieved R² = 0.XX with 5-fold cross-validation
- Created professional visualizations and reports

**Skills demonstrated:**
- Data cleaning & preprocessing (dplyr)
- Exploratory Data Analysis
- Feature engineering
- Statistical modeling
- Data visualization (ggplot2, corrplot)
- Reproducible research

**Tools:** R, dplyr, ggplot2, corrplot, jsonlite
```

---

### 🚀 Quick Command Cheat Sheet

```bash
# Clone repo (if working with team)
git clone https://github.com/your-username/tmdb-ratings-analysis.git
cd tmdb-ratings-analysis

# Create new repo
git init

# Check status
git status

# Add files
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub
git push origin main

# Pull latest changes
git pull origin main
```

---

### ⏱️ Timeline

| Task | Time | Status |
|------|------|--------|
| Setup R & RStudio | 5 min | ⬜ |
| Download Dataset | 5 min | ⬜ |
| Setup Project Folder | 3 min | ⬜ |
| Run Analysis | 15 min | ⬜ |
| Review Results | 5 min | ⬜ |
| Push to GitHub | 5 min | ⬜ |
| **TOTAL** | **~40 min** | |

---

### 📞 Support Resources

If you get stuck:
1. Check script console output (detailed error messages)
2. Review README.md (Troubleshooting section)
3. Check Kaggle dataset page (data format issues)
4. Search StackOverflow (R/tidyverse errors)
5. Ask professor (conceptual questions)

---

**Good luck with your project! 🎓**

For questions, check the README.md or contact: yash.yadav@example.com
