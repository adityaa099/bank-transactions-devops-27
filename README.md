Bank Transaction Processing – DevOps Assignment

This project demonstrates Linux automation tasks, file extraction, archiving, and GitHub-based branching workflow for maintaining transaction logs.

📂 Project Structure
bank/
│
├── transactions/
│   └── day1.log                # Contains 14+ banking transactions
│
├── reports/
│   └── credit.txt              # Extracted list of Credit transactions
│
├── archive/
│   └── reports_backup.tar.gz   # Archived backup of reports directory
│
└── README.md

🛠️ Part A – Linux Task Execution
✔️ 1. Created banking directory structure
bank/{transactions,reports,archive}

✔️ 2. Created day1.log containing:

Transaction ID

Amount

Type (Credit/Debit)

✔️ 3. Extracted all “Credit” transactions
grep "Credit" transactions/day1.log > reports/credit.txt

✔️ 4. Counted total lines and words in credit.txt

Lines:

wc -l reports/credit.txt


Words:

wc -w reports/credit.txt


Both (lines, words, bytes):

wc reports/credit.txt

✔️ 5. Archived reports folder into reports_backup.tar.gz
tar -czvf archive/reports_backup.tar.gz reports

🔀 Part B – GitHub Implementation
✔️ 1. Initialized Git repository
cd bank
git init

✔️ 2. Added .gitignore to ignore archive files
*.tar.gz

✔️ 3. Committed initial transaction logs
git add .
git commit -m "Initial commit – banking transaction logs"

✔️ 4. Created branch report-update and added new transaction
git checkout -b report-update
echo "T015,5000,Credit" >> transactions/day1.log
git add transactions/day1.log
git commit -m "Added new transaction entry"
git push -u origin report-update

✔️ 5. Created Pull Request on GitHub

Merged report-update → main successfully.

🚀 Tools Used

Linux Terminal

Git & GitHub

grep, wc, tar

Branching & Pull Request workflow

✨ Author

Aditya Chouksey 
DevOps Student
