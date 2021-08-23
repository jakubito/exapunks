<img src="histogram.png" width="400" />

---

**XA**

```
LINK 800
GRAB 200
COPY F X
WIPE
LINK 800
MAKE

MARK LOOP
COPY X F
SUBI X 1 X
TEST X = -1
FJMP LOOP
```
