<img src="histogram.png" width="400" />

---

**XA**

```
GRAB 300
LINK 800

REPL COUNTER

MARK DIAL
COPY -1 #DIAL

@REP 11
COPY F #DIAL
@END

REPL WORKER
ADDI X 11 X
TEST MRD
FJMP DIAL

MODE
COPY 1 M
MODE

VOID M
SEEK 9999

MARK WRITE
@REP 11
COPY M F
@END

NOOP
NOOP
TEST MRD
TJMP WRITE

SEEK -9999
SEEK X
JUMP DIAL

MARK WORKER
LINK 800
COPY 1 M
GRAB 200

MARK READ
SEEK 1

@REP 11
COPY F M
@END
JUMP READ

MARK COUNTER
MODE

MARK LISTEN
ADDI X M X
TEST X = 8
FJMP LISTEN

KILL
GRAB 300
WIPE
LINK 800
KILL
```
