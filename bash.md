### Loop through lines of a file

```bash
while read theLine || [[ -n $theLine ]]; do
	echo "$theLine"

done < "<THE_FILE_NAME>"
```

### ! commands

```bash
# Last parameter from previous command
!$

# All params from previous command
!*
```

## truncate file

```bash
> '<PATH_TO_FILE>'
```