This is part 1 of w2

## Observation (Step A3)
Trên nhánh main, week2.md KHONG chua cac dong da them o nhanh week2
("working 1 change", "working 2 change", "This line only exists on week2 branch")
vi cac commit do chi ton tai rieng tren nhanh week2, chua duoc merge vao main.

working 1 change

working 2 change
This line only exists on week2 branch

## Step B2 - Branch merge status
# git branch --merged
* main
  week2b
# git branch --no-merged
  wip

## Step D4 - What rebase did
git rebase main (chay tren nhanh experiment) da lay 2 commit rieng cua
experiment ("Add file1...", "Add file2...") va "phat lai" (replay) chung
len tren dinh cua nhanh main hien tai (sau commit "Add file3 on main").
Ket qua: lich su cua experiment gio thanh mot duong thang (linear) noi
tiep main, khong con la nhanh re nhu truoc rebase. Day khac voi merge -
merge se tao them 1 commit merge moi va giu nguyen lich su re nhanh cu.