# Create New Package

## Command

```sh
$ cd ~/catkin_ws/src/
$ catkin_create_pkg package_name
```

## After creating

e.g.

```sh
$ catkin_create_pkg my_package
```

+ have 2 files under package

```
catkin_ws/
    src/
        my_package/             ← your package
            CMakeList.txt
            package.xml
```

## Work with git repository

Ref: [git strategy for catkin and package folders](https://answers.ros.org/question/257855/git-strategy-for-catkin-and-package-folders/)

```
catkin_ws/
    src/
        git_repo_name/          ← your git repository
            my_package/         ← your package
                CMakeList.txt
                package.xml
```

### More than one package under git repo
```
catkin_ws/
    src/
        git_repo_name/          ← your git repository
            my_package1/        ← your package
                CMakeList.txt
                package.xml
            my_package2/        ← your package
                CMakeList.txt
                package.xml
            my_package3/        ← your package
                CMakeList.txt
                package.xml
```
