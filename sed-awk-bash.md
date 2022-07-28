```bash
sed 's/Nick/John/g' report.txt > report_new.txt
sed 's/Nick|nick/John/g' report.txt
sed 's/^/ /' file.txt >file_new.txt
sed -n '/Of course/,/attention you pay/p' myfile
sed -n 12,18p file.txt
sed 12,18d file.txt
sed G file.txt #Double-space file.txt
sed -f script.sed file.txt
sed '5!s/ham/cheese/' file.txt
sed '$d' file.txt
sed '/[0-9]\{3\}/p' file.txt
sed '/boom/!s/aaa/bb/' file.txt
sed '17,/disk/d' file.txt
echo ONE TWO | sed "s/one/unos/I"
sed 'G;G' file.txt #Triple-space a file

sed = file.txt | sed 'N;s/\n/\t/'
sed '/regex/{x;p;x;G;}' file.txt
sed '/regex/G' file.txt
```
1. (*) tries to a get you the longest match possible it can detect.

```bash
awk '//{print}'/etc/hosts
awk '/[al1]/{print}' /etc/hosts
awk '/^fe/{print}' /etc/hosts
awk '/ab$/{print}' /etc/hosts

```

```bash
grep -i "the" demo_file

```
