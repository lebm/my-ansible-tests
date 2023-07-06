# My ansible tests

Watching ansible oreilly tutorials

## Assorted useful commands  
> Update outdated python packages  
```
pip install -U $(pip list -o | tail -n +3 | cut -f1 -d' ')
```
