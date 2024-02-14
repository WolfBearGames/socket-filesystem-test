# A Socket Runtime Filesystem Test failing on Linux

1. Please paste a valid file path to a .txt file into the text input field (the file might get overwritten, be careful)
2. click "load file"
3. You will see a line "File path is: ..." in the console
4. You will also see a line "FileHandle is not opened" in the console. The file could not be opened
5. type some text into the text area
6. click "save to file"
7. You will the "save button clicked" in the console", but not the the line after the writeFile method "text saved to.."
8. even though the text has been saved to the file overwriting anything written from the beginning of the file

## Problems

* the file cannot be opened
* saving works only halfway, because the app gets stuck at the "await fs.writeFile(filepath.value, textarea.value);" line and does not execute the console.log in the next line

## Platform

Linux nobara-mini 6.7.0-204.fsync.fc39.x86_64 #1 SMP PREEMPT_DYNAMIC TKG Wed Jan 17 09:24:55 UTC 2024 x86_64 GNU/Linux

## Socket Version

0.5.4 (f90ba121)

# Build instructions

1. Install the Socket SDK compiler following instructions [here](https://socketsupply.co/guides/#install).
2. Run the application with `ssc build -r`.
