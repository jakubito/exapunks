<img src="histogram.png" width="400" />

---

**XA**

```
LINK 800

REPL MUSCLE_CLONE
LINK 3
LINK 3
REPL HEAT
NOOP
JUMP RECEIVE

MARK MUSCLE_CLONE
LINK -3
LINK -3
REPL HEAT_CLONE
NOOP
JUMP SEND

MARK HEAT
LINK 3
REPL PRESSURE
JUMP SEND

MARK HEAT_CLONE
LINK -3
REPL PRESSURE_CLONE
JUMP RECEIVE

MARK PRESSURE
LINK 3
JUMP SEND

MARK PRESSURE_CLONE
LINK -3
JUMP RECEIVE

MARK SEND
COPY #NERV M
JUMP SEND

MARK RECEIVE
COPY M #NERV
NOOP
JUMP RECEIVE
```
