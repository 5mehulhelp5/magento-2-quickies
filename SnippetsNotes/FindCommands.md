# All commands/shortcuts for finding/searching texts
## Linux/Github/SublimeText search

**Sublime Text Find**
```sh
```

**VS Code Find**
```sh
```

**search commit message**
```sh
git log --all --grep='texttosearch' 
```


**Linux Text Find**
```sh
#Magento 2 : Find cacheable="false" cache tag 
find vendor app -regextype 'egrep' -type f -regex '.*/layout/.*\.xml' -not -regex '.*(vendor/magento/|/checkout_|/catalogsearch_result_|/dotmailer).*' | xargs grep --color -n -e 'cacheable="false"'

#Cli : Linux find string in folder #CLI
grep -rnw '/path/to/somewhere/' -e 'pattern' 
grep -rnw '/path/to/somewhere/' -e 'pattern' | grep -v 'ignore'

grep -ril 'TexttoSearchInappfolder' app

#filename
grep -rnwl '/path/to/somewhere/' -e 'pattern'
```

**Github Search**
```sh
"
#reload source
source ~/.bashrc
```
