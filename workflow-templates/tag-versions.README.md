# tag-versions

## Setup
Create a [new repo](https://github.com/new) and then clone it locally, then run the following:
```
$tagPrefix = "v"
$firstVersion = "1.0.0.0"

$fulltag = "$($tagPrefix)$($firstVersion)"
git tag -a $fulltag
git push origin $fulltag
```

## Adding the action
Go to the repo you created and select "Actions" from the header bars. Scroll down until you see the FaceFirst-Engineering actions.

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
