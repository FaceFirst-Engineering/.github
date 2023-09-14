# tag-versions

## Setup
Create a new repo and then clone it locally, then run the following:
```
$tagPrefix = "v"
$firstVersion = "1.0.0.0"

$fulltag = "$($tagPrefix)$($firstVersion)"
git tag -a $fulltag
git push origin $fulltag
```

## to quickly test commits
```
$branch = "test-minor"
$default = "dev"
git checkout -b $branch
echo "test" > test.txt
git add test.txt
git commit -am "nothing"
rm test.txt
git add test.txt
git commit -am "nothing"
echo "test" > test.txt
git add test.txt
git commit -am "nothing"
rm test.txt
git add test.txt
git commit -am "four commits"
git checkout $default
git merge $branch 
```
