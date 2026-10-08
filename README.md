<!-- ========================================================= -->
<!--                    ✦ ANIMATED HEADER ✦                   -->
<!-- ========================================================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1026,35:6C5CE7,70:FF8FC7,100:8BE9FD&height=180&section=header&animation=twinkling" width="100%"/>
</p>

<br>

<!-- ========================================================= -->
<!--                    ✦ NAME ANIMATION ✦                    -->
<!-- ========================================================= -->

<p align="center">
  <img
    src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=42&duration=2800&pause=900&color=B9A7FF&center=true&vCenter=true&width=700&height=90&lines=YOUR+NAME;aka+the+girl+who+debugs+at+2AM"
    alt="Animated Name"
  />
</p>

<p align="center">
  <img
    src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=2500&pause=800&color=8BE9FD&center=true&vCenter=true&width=650&height=50&lines=Computer+Science+Student+%7C+Data+%26+Code;Building+things+I+probably+shouldn't+be+able+to;currently+turning+coffee+into+commits+%E2%98%95"
    alt="Animated Introduction"
  />
</p>

<br>

---

<!-- ========================================================= -->
<!--                       ✦ WHO AM I ✦                        -->
<!-- ========================================================= -->

## `whoami.exe`

<table>
<tr>

<td width="60%" valign="top">

### Hey, I'm **SAMRIDDHI** 👾

I'm a **Computer Science student specializing in Data Science**, 
who enjoys turning random ideas into actual working projects.

I like understanding **how things work**, breaking them,
fixing them, and occasionally pretending the bug was intentional.

### ✦ Currently interested in

text
⌁ Data Science
⌁ Machine Learning
⌁ Frontend Development
⌁ DSA & Problem Solving
⌁ AI-powered applications
⌁ Building weird little projects

✦ My current philosophy

"If it works, don't touch it.
If it doesn't work... touch everything."

</td> <td width="40%" align="center"> <img src="assets/kitty.gif" width="220">

<br><br>
╭────────────────────╮
│  STATUS: ONLINE    │
│  MOOD: CAFFEINATED │
│  BUGS: MANY        │
│  FIXED: eventually │
╰────────────────────╯
<p align="center"> <img src="assets/kitty.gif" width="160"> </p> <p align="center">
"I don't have imposter syndrome."
"I have compiler errors."
</p> <p align="center">

☕ coffee → 💻 code → 🐛 bug → 😭 debug → ✨ somehow works

</p> <br>
name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg?color_snake=%23FF9FCB&color_dots=%230D1026,%23B9A7FF,%239B7CFF,%23FF9FCB,%238BE9FD

      - uses: crazy-max/ghaction-github-pages@v4
        with:
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
