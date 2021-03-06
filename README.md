# Take Me To Develop!
 
## ABOUT
This tool detects a release branch you're on (of the form release-M.mm.0),
and merges it to all future release branches and then to develop.
for example, if you're on release-2.52.0, and you run the tool, it should perform these merges:
```
    checkout release-2.53.0
    pull release-2.53.0
    merge release-2.52.0 -> release-2.53.0
    push release-2.53.0
    checkout develop
    pull develop
    release-2.53.0 -> develop
    push develop
```
In case of a conflict or other git errors, it will stop and let you deal with it.

## INSTALLATION
* Clone the repo somewhere:
```
git clone git@github.com:wat-izz/take_me_to_develop.git
```
* Run setup.py install:

```
cd take_me_to_develop/
python setup.py install
```

## USAGE
Just run it inside the repo, with a release branch you want to merge checked out.
```
cd your/repo/
take-me-to-develop
```

## AUTHOR
Adam Narkunski


## LICENSE

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file.

