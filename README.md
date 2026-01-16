# quick-bash-hacks

## extract dependencies from `go.mod`

```bash
find . -type f -name go.mod -exec cat {} + | grep -oE 'github\.com/[^[:space:]]+' | sort -u | sed 's\^\https://\'
```
