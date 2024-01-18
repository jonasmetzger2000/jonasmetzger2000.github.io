# Skripte

```bash
o() {
    if git config --get remote.origin.url > /dev/null ; then
        open $(git config --get remote.origin.url | sed "s/git@\(.*\):\(.*\).git/https:\/\/\1\/\2\//")
    else
        echo "This is not an git repo.."
    fi
}
```