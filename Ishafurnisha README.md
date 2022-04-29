- 👋 Hi, I’m @Agiisha
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Agiisha/Agiisha is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#!/usr/bin/bash

# Configuration stuff

fspec=qq.c
num_files=6

# Work out lines per file.

total_lines=$(wc -l <${fspec})
((lines_per_file = (total_lines + num_files - 1) / num_files))

# Split the actual file, maintaining lines.

split --lines=${lines_per_file} ${fspec} xyzzy.

# Debug information

echo "Total lines     = ${total_lines}"
echo "Lines  per file = ${lines_per_file}"    
wc -l xyzzy.*
OUTPUT :
Total lines     = 70
Lines  per file = 12
  12 xyzzy.aa
  12 xyzzy.ab
  12 xyzzy.ac
  12 xyzzy.ad
  12 xyzzy.ae
  10 xyzzy.af
  70 total
