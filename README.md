# awk-examples

> Collection useful AWK examples

## Examples


```
awk 'BEGIN { print "hello world" }' <<EOF
foo
bar
baz
EOF
hello world
```

```
awk '{ print }' <<EOF
foo
bar
baz
EOF
foo
bar
baz
```

```
awk '{ if ($0 ~ /^f/) { print "cats" } else { print "dogs" } }' <<EOF
foo
bar
baz
EOF
cats
dogs
dogs

awk '/^f/ { print "cats"; next } { print "dogs" }' <<EOF
foo
bar
baz
EOF
cats
dogs
dogs
```

```
awk '{ gsub(/^f.*$/, "flapjacks"); print }' <<EOF
foo
bar
baz
EOF
flapjacks
bar
baz
```
