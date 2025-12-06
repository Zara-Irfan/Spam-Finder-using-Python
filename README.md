# Gmail Takeout Spam Scanner – README
Overview

This project automatically scans a Google Takeout Mail export and extracts spam emails from the archive.
It works even if your Takeout contains:

MBOX files

HTML-only exports

Mixed folder structures

If no spam emails are found, the tool clearly reports “No spams found.”

All extracted text, full reports, and spam-only results are saved as output files.

Features

Automatically detects your latest Takeout ZIP in the Downloads folder.

Extracts ZIP into a clean working directory.

Supports reading:

Google MBOX files

Takeout HTML archives

Identifies emails marked as Spam or containing spam-like text.

Saves:

Cleaned email text

Full extraction report

Spam-only file

Shows clear status messages during every step.

Works on any Takeout structure (handles Google’s inconsistent folder naming).

Input Requirements

A Gmail Takeout ZIP file downloaded from takeout.google.com

Python installed on your machine

Place the ZIP file in your Downloads folder before running the script.

Output Files

After running, you will get:

File	Purpose
cleaned_takeout_emails.txt	All extracted email text
takeout_full_report.txt	Detailed extraction log
spam_results.txt	Only spam emails
“No spams found”	Printed if spam list is empty
How It Works

The script searches your system for the newest Takeout ZIP.

ZIP is extracted into a working directory (TakeoutMail).

The tool searches for:

.mbox files

.html files

Emails are parsed and cleaned.

Spam is detected using:

Gmail’s “Spam” folder name

Common spam keywords

Results are saved automatically.

Spam Detection Rules

An email is marked as spam if:

It comes from Gmail’s Spam or Trash folders in the Takeout

It contains strong spam indicators (keywords, promotional patterns)

The email metadata suggests it was originally categorized by Google as spam

It matches basic content-based spam heuristics

Why This Project Exists

Google Takeout often creates:

Different folder structures

Missing MBOX files

Multiple ZIP chunks

HTML-only archives

This tool handles all irregular formats and still extracts usable email + spam data.

Limitations

Cannot restore actual Gmail labels if your Takeout lacks them

HTML exports may not contain full email bodies

Spam detection works best with MBOX exports
