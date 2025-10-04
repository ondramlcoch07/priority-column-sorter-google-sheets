# Google Sheets Priority Sort

Automatically sorts Google Sheets columns based on **priority instructions in row 2**. Supports multi-column sorting, ascending/descending order, and keeps the **active cell on its row** after sorting. Built with help from ChatGPT (OpenAI).

---

## Features
- Multi-column sorting by priority (defined in row 2).  
- Ascending (`A-Z`) or descending (`Z-A`) per column.  
- Automatically triggers on edits (except row 2).  
- Active cell moves with its row after sorting.  
- Fully configurable via row 2 instructions, no script changes needed.

---

## Installation
1. Open your Google Sheet.  
2. Go to **Extensions → Apps Script**.  
3. Delete any existing code and paste the [script]([https://openai.com](https://github.com/ondramlcoch07/priority-column-sorter-google-sheets/blob/main/code)).
5. Save the project.  

---

## Usage
1. Add sorting instructions in **row 2**, one per column. Format example:
- **Number** = priority (1 = highest)  
- **A-Z** = ascending, **Z-A** = descending  
2. Enter or edit data starting from **row 3**.  
3. The sheet will auto-sort based on the instructions.  
4. The active cell will remain on its row after sorting.

---

## Example

**Row 2 Instructions:**  
**Before Sorting (Row 3 and below):**

| Name  | Score |
|-------|-------|
| John  | 85    |
| Alice | 90    |
| Bob   | 75    |
| Alice | 80    |

**After Sorting:**

| Name  | Score |
|-------|-------|
| Alice | 90    |
| Alice | 80    |
| Bob   | 75    |
| John  | 85    |

**Explanation:**  
- First, sort by **Name (column 1)** ascending → Alice, Alice, Bob, John  
- Then, within the same Name, sort by **Score (column 2)** descending → Alice 90 before Alice 80  

---

## Notes
- Only edits **outside row 2** trigger sorting.  
- Ensure row 2 instructions are correctly formatted (`number. A-Z/Z-A`).  
- Works best for sheets with data starting at row 3.  

---

**Made with assistance from [ChatGPT](https://openai.com).**
