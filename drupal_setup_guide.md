# Drupal 9 Setup Guide (Windows/XAMPP + PostgreSQL)

**Objective:** Install Drupal 9 on a modern XAMPP (PHP 8.2) environment using PostgreSQL.
**Prerequisites:** XAMPP, DBeaver, Git Bash, Composer.

---

## Step 1: The "Surgery" (Configure XAMPP)
*Why: XAMPP disables PostgreSQL and Image handling by default. We must enable them.*

1. Open **XAMPP Control Panel**.
2. Click **Config** (next to Apache) -> Select **`PHP (php.ini)`**.
3. Press `Ctrl + F` to search and **remove the semicolon (;)** from the start of these lines:
   ```ini
   extension=gd
   extension=pdo_pgsql
   extension=pgsql