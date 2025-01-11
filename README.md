# JupyterLab + GitHub Workflow

This repository follows a structured workflow that integrates **JupyterLab**, **GitHub**, and **virtual environments** to ensure organized development, version control, and reproducibility.

## 🚀 Workflow Overview
This workflow ensures efficient management of Jupyter Notebooks while keeping the project dependencies isolated using virtual environments.

---
## **1️⃣ Setting Up the Project**
Before starting work, navigate to your project directory and activate the virtual environment.

```sh
cd /c/Users/mieraci/JupyterLabEnv  # Navigate to the project folder
source venv/Scripts/activate  # Activate the virtual environment (Git Bash)
# For Windows CMD, use: venv\Scripts\activate
```

Launch JupyterLab:
```sh
jupyter lab
```

---
## **2️⃣ Version Control with Git**
### **Checking the Git Status**
Before committing changes, check which files have been modified:
```sh
git status
```

### **Adding and Committing Changes**
After making changes in JupyterLab, stage and commit your work:
```sh
git add .
git commit -m "Updated Jupyter Notebook"
```

### **Pushing Changes to GitHub**
Upload your latest work to GitHub:
```sh
git push origin main
```

---
## **3️⃣ Syncing with GitHub**
Before making any changes, ensure you have the latest updates from the remote repository:
```sh
git pull origin main
```
If there are conflicts, resolve them before proceeding.

---
## **4️⃣ Managing Dependencies**
To maintain reproducibility, store project dependencies in `requirements.txt`.

### **Installing a New Package**
```sh
pip install package_name
pip freeze > requirements.txt
```
Commit the updated `requirements.txt` to GitHub:
```sh
git add requirements.txt
git commit -m "Updated dependencies"
git push origin main
```

### **Setting Up the Project on a New Machine**
To recreate the environment:
```sh
python -m venv venv  # Create virtual environment
source venv/Scripts/activate  # Activate it
pip install -r requirements.txt  # Install dependencies
```

---
## **5️⃣ Best Practices**
- **Use `git status` before committing** to ensure you're tracking the right files.
- **Keep `.gitignore` updated** to avoid unnecessary files (e.g., `.ipynb_checkpoints/`, `venv/`).
- **Push changes frequently** to avoid losing work.
- **Always pull updates** before starting new work.

---
## **📌 Quick Reference Table**
| Step | Command | Purpose |
|------|---------|---------|
| **Start project** | `cd /c/Users/mieraci/JupyterLabEnv && source venv/Scripts/activate && jupyter lab` | Open Jupyter environment |
| **Check Git status** | `git status` | See what changed |
| **Commit changes** | `git add . && git commit -m "Updated Notebook"` | Save changes in Git |
| **Push to GitHub** | `git push origin main` | Backup code on GitHub |
| **Pull updates** | `git pull origin main` | Sync with GitHub if working across devices |
| **Install dependencies** | `pip install package_name && pip freeze > requirements.txt` | Manage project packages |
| **Recreate env on a new machine** | `pip install -r requirements.txt` | Install all dependencies |

---
### **🎯 Final Notes**
By following this workflow, you ensure:
✅ Organized project management 🚀  
✅ Version-controlled Jupyter Notebooks 📁  
✅ Reproducible environments 🔧  

If you need further automation, consider using **GitHub Actions** for continuous integration! 🎯

