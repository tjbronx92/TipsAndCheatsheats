# SED - Stream Editor

Delete a range of lines:
```bash
# Deletes lines 1-3 in file
sed "1,3d" [input_file]
```

Perform Consecutive Substitutions:
- add the script to the commands to be executed
> -e script, --expression=script

```bash
echo catdog | sed -e "s/c/C/" -e "s/d/D"
```
