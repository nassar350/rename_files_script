# Rename Files Script

## 📌 Overview

The `rename_files_script` is a Bash script that automates file renaming in a given directory and its subdirectories based on various options. It ensures efficient renaming while preventing data loss.

## 🚀 Features

- Search for files in a specified directory
- Rename files with a new name
- Add prefixes or suffixes
- Convert filenames to lowercase or uppercase
- Replace spaces with underscores
- Ensure no duplicate names
- Maintain a log of renaming history

## 🔧 Usage

```
./rename_files_script [Options] [Arguments][Optional]
```

### 📌 Options

| Option          | Description                                     |
| --------------- | ----------------------------------------------- |
| `-P <path>`     | Specify the directory to search in              |
| `-f <old_file>` | Provide the old filename to rename              |
| `-r <old:new>`  | Rename the old filename to a new name           |
| `-p <prefix>`   | Add a prefix before the filename                |
| `-s <suffix>`   | Add a suffix after the filename                 |
| `-l`            | Convert filename to lowercase                   |
| `-u`            | Convert filename to uppercase                   |
| `-S`            | Replace spaces in the filename with underscores |
| `-h`            | Display the usage menu                          |

## 🔄 Examples

1️⃣ **Rename a file**:

```bash
./rename_files_script -P /home/user/docs -f old.txt -r new.txt
```

🔹 \*Renames **`old.txt`** to **`new.txt`** in \**`/home/user/docs`*

2️⃣ **Add a prefix**:

```bash
./rename_files_script -P /home/user/docs -f report.txt -p FINAL_
```

🔹 \*Changes **`report.txt`** to \**`FINAL_report.txt`*

3️⃣ **Add a suffix**:

```bash
./rename_files_script -P /home/user/docs -f report.txt -s _FINAL
```

🔹 \*Changes **`report.txt`** to \**`report_FINAL.txt`*

4️⃣ **Convert filename to lowercase**:

```bash
./rename_files_script -P /home/user/docs -f MyFile.TXT -l
```

🔹 \*Changes **`MyFile.TXT`** to \**`myfile.txt`*

5️⃣ **Convert filename to uppercase**:

```bash
./rename_files_script -P /home/user/docs -f myfile.txt -u
```

🔹 \*Changes **`myfile.txt`** to \**`MYFILE.TXT`*

6️⃣ **Replace spaces with underscores**:

```bash
./rename_files_script -P /home/user/docs -f "my file.txt" -S
```

🔹 \*Changes **`my file.txt`** to \**`my_file.txt`*

## 📝 Logging Renaming History

- All renaming operations are recorded in a log file.
- The log file stores details including timestamps, old filenames, new filenames, and operations performed.
- Example log entry:
  ```
  [2025-03-22 14:30:00] Renamed: old.txt → new.txt
  ```
- The log file can be reviewed to track past renaming actions and prevent accidental overwrites.
- The log file path will be in ```/var/log/rename.log```

## ⚠️ Notes

- The script prevents duplicate filenames to avoid overwriting existing files.
- Ensure you have the necessary permissions to rename files in the target directory.
- If `-P` is not specified, the script will search for files in the current directory by default.
- You can use ```bash``` instead of ```./``` for running the script.

## 📜 License

This script is open-source and available under the MIT License.

---

💡 **Tip:** Always test with a backup before batch renaming files!
