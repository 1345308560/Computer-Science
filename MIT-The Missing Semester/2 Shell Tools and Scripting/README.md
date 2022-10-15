# Shell Tools and Scripting
1. Read man ls and write an ls command that lists files in the following manner
```shell
man ls
ls -all
ls -all -h
ls -all -h -t
ls -all -h -t --color=auto
```
2. Write bash functions marco and polo that do the following. 
```shell
# marco.sh
marco(){
    echo $(pwd) > /tmp/missing/marco_path.txt
}
```
```shell
# polo.sh
polo(){
    cd "$(cat /tmp/missing/marco_path.txt)"
}

```
3. Say you have a command that fails rarely. In order to debug it you need to capture its output but it can be time consuming to get a failure run. 
```shell
for((count=1;;count++))
do
 	bash /tmp/missing/buggy.sh 2> test.log
 	if [[ $? -eq 1 ]]; then
 		echo "It take $count steps."
  		break
 	fi
done
```

4. Your task is to write a command that recursively finds all HTML files in the folder and makes a zip with them. Note that your command should work even if the files have spaces (hint: check -d flag for xargs).
```shell
find . -type f -name "*.html" | xargs -d '\n'  tar -cvzf html.zip
```