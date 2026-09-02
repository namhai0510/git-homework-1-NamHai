## PART A - Q1
New-Item week2.md
code week2.md
git add week2.md
git commit -m "Add week2.md"
git branch week2
git checkout week2
git branch

## PART A - Q2
Add-Content week2.md "`nworking 1 change"
git add week2.md
git commit -m "working 1"

Add-Content week2.md "`nworking 2 change"
git add week2.md
git commit -m "working 2"

## PART A - Q3
Add-Content week2.md "`nThis line only exists on week2 branch"
git add week2.md
git commit -m "Add unique line on week2"
git checkout main

## Observation (Step A3)
Trên nhánh main, week2.md KHONG chua cac dong da them o nhanh week2
("working 1 change", "working 2 change", "This line only exists on week2 branch")
vi cac commit do chi ton tai rieng tren nhanh week2, chua duoc merge vao main.

git add week2.md
git commit -m "Document findings about week2.md on main"

## PART A - Q4
git checkout -b week2b
git merge week2

## Observation (Step A4)
Xuat hien conflict
Auto-merging week2.md
CONFLICT (content): Merge conflict in week2.md
Automatic merge failed; fix conflicts and then commit the result.

# Su dung VS code de tinh chinh noi dung
git add week2.md
git commit -m "Merge branch 'week2' into week2b"

git branch -d week2
git branch
git log --oneline --graph --all

## PART B - Q1
git checkout main
git checkout -b wip
New-Item wip.txt
git add wip.txt
git commit -m "Add wip.txt"

git checkout main
git merge week2b

git branch

## PART B - Q2
git branch --merged
git branch --no-merged

git add week2.md
git commit -m "Document merged/unmerged branches"

## PART B - Q3
git branch -d week2b

## PART B - Q4
git branch -m wip work-in-progress
git push origin -u work-in-progress
git push origin --delete wip 
# Thu xoa wip tren remote nhung khong ton tai
git branch -a

## PART C - Q1
git checkout work-in-progress
Add-Content wip.txt "`nSome progress notes here"
git add wip.txt
git commit -m "Update wip.txt"
git push

## PART C - Q2
git branch -vv
  main             a31289c [origin/main: ahead 7] Document merged/unmerged branches
* work-in-progress 710fa61 [origin/work-in-progress] Update wip.txt

## PART C - Q3
Tao PR work-in-progress -> main qua GitHub UI
https://github.com/namhai0510/git-homework-1-NamHai/pull/1

## PART D - Q1
git checkout main
git checkout -b experiment

New-Item file1.txt
git add file1.txt
git commit -m "Add file1 on experiment"

New-Item file2.txt
git add file2.txt
git commit -m "Add file2 on experiment"

## PART D - Q2
git checkout main
New-Item file3.txt
git add file3.txt
git commit -m "Add file3 on main"

## PART D - Q3
git checkout experiment
git rebase main

## PART D - Q4
git checkout main
code week2.md

git add week2.md
git commit -m "Explain rebase result"