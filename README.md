# N-Queens-Puzzle

This project is an advanced and interactive version of the classic N-Queens Puzzle, enhanced with:

🎨 Randomly generated colored regions (blobs)

🔍 Real-time conflict detection

🚫 Striped conflict highlighting

🤖 Auto-solver based on region constraints

🖱️ Interactive GUI using Python Tkinter

🔄 Resizable board (4×4 to 12×12)

The objective remains the same:
Place N queens such that no two queens attack each other — but with an additional twist: only one queen is allowed per region!

🚀 Features
✔️ Interactive GUI

Click to place/remove queens.

Real-time updates with visual conflict highlighting.

Nice color-coded region display.

✔️ Region-Based N-Queens

The grid is partitioned into N colored connected regions.

Regions are irregular blob-like shapes.

Each region may contain at most one queen.

✔️ Conflict Highlighting

Conflicts are shown with red diagonal stripes for:

Row conflicts

Column conflicts

Diagonal conflicts

Region conflicts

✔️ Auto Solver

Click Auto Solve to automatically place queens with the rule:

One queen per row

One queen per column

One per main diagonal

One per anti-diagonal

One per region

✔️ Dynamic Board Size

Choose sizes from 4×4 up to 12×12:

Regions regenerate every time you change size.

Guaranteed solvable region partitions are generated.

🖥️ How to Run
Requirements

Python 3.x

Tkinter (included by default in most Python installations)

Run the app
python your_file_name.py


The Tkinter window will open automatically.

🧩 Controls
Button	Function
Check Solution	Detects conflicts and highlights them
Auto Solve	Uses backtracking + region constraints to solve
Reset	Clears all queens
New Regions	Generates a new colored region partition
Board Size	Dropdown to change board from 4×4 to 12×12

Clicking on a cell places/removes a queen.

🧠 How It Works (Brief)
1. Region Generation

generate_blob_regions(n)
Creates N connected, irregular regions on an n × n grid using randomized multi-source BFS.

2. Conflict Detection

Checks conflicts in:

Row

Column

Major diagonal (r-c)

Minor diagonal (r+c)

Region (only one queen allowed)

3. Solver

solve_with_colors(region)
Backtracking-based solver that ensures:

No row/column/diagonal conflict

No region conflict

4. Conflict Visualization

Uses Liang–Barsky line clipping algorithm to draw red diagonal stripes only inside conflicted squares.

📁 File Overview
main.py (or your filename)
├── QueensApp class
├── Region generation
├── Solver
├── Conflict detection
└── Tkinter GUI

🎨 Screenshot (Optional)

You can insert images here:

![App Screenshot](screenshot.png)

🛠️ Future Improvements

Export board as image

Add timer or challenge mode

Add region editing tools

📜 License

This project is free to use and modify for educational or personal purposes.
