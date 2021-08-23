<img src="histogram.png" width="400" />

---

**XA**

```
GRAB 300
LINK 800

MARK LOOP
COPY F M
TEST EOF
FJMP LOOP

WIPE
KILL
```

**XB**

```
LINK 800
GRAB 200
SEEK 9999

MARK LOOP
COPY M F
JUMP LOOP
```
