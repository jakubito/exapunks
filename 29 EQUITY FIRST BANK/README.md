<img src="histogram.png" width="400" />

---

**XA**

```
GRAB 301
COPY F X
COPY F M
DROP

GRAB 300
SEEK 9999
LINK 800

MARK LISTEN
COPY M F
COPY X F
COPY 1 F
COPY 0 F

@REP 4
NOOP
@END

TEST MRD
TJMP LISTEN

LINK 800
KILL
KILL
DROP
GRAB 199
SEEK 9999
COPY 300 F
```

**XB**

```
GRAB 300
COPY F X
DROP

COPY M T
LINK 800
LINK 800

GRAB 199
MODE

REPL WORKER
REPL WORKER

MARK LOOP
COPY F M
VOID M
JUMP LOOP

MARK WORKER
GRAB M

MODE
COPY F M
MODE
COPY 1 M

SEEK 9999
COPY X F
COPY T F
COPY 1 F
COPY 0 F

DROP
JUMP WORKER
```
