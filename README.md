# commission-charter
The semi-official charter for Thursday commissions

## Contibuting

These need fixing:

> :boom: `<some task>`

Make a pull request :heart:


## Attendance Score

Before every commission, a poll is realeased to commission members.
The poll has the following options:
* hard yes
* soft yes
* soft no
* hard no

Poll registrations and commission attendance are recorded.

An attendance score is computed for each member.

Exponential moving average weigh recent attendance more heavily.

> :boom: how often?

The score

## Location

### Hard Criteria
Location should fulfill all **hard criteria**:
* outdoor seating
* heat lamps (during winter months)
* room for our own table

## Location Score

If a location fulfills all hard criteria the location can be marked
For each attendant, $c$, their:
* $L_{pre}$, Pre-commission location (i.e. $c$'s work)
* $L_{commission}$ - Comission location (is same for all attendees)
* $L_{post}$ - Post-commission location (i.e. $c$'s home) L_post

> :boom: the terms $L_{pre}$, $L_{commission}$, $L_{post}$ are a little sucky,
> can we think of something better?

The location score is computed by taking the sum of distances for all members:

```math
\sum_{i=0}^{N} D_{L_{pre_{i}} \rightarrow L_{commission}} +  D_{L_{comission} \rightarrow L_{post_{i}}}
```

Where $D_{a \rightarrow b}$ is distance (as the crow flies) from $a$ to $b$[^1]


### One-Dimensional Example
Consider the __simple thursday commission universe__ (STCU) which:
* consists of six locations on a straight line
* contains three commission members

| Member | $L_{pre}$ | $L_{post}$ | Attendance score $a$ |
| -      | -         | -          | -                    |
| $c_1$  | 1         | 5          | .5                   |
| $c_2$  | 2         | 6          | .2                   |
| $c_3$  | 3         | 1          | .8                   |

Consider a bar located at $L_{commission} = 3$.
The locations score of the bar is...

> :boom:


```math
S = \sum_{i=0}^{N} D_{L_{pre_{i}} \rightarrow L_{commission}} +  D_{L_{comission} \rightarrow L_{post_{i}}}
```

> :boom: align above maths equations?


$$ \begin{align} 2x - 4 &= 6 \\ 2x &= 10 \\ x &= 5 \end{align} $$

$$ \begin{align} 2x - 4 &= 6 \\ 2x &= 10 \\ x &= 5 \end{align} $$

> :boom: is above maths equation aligned?

## Rounds
Attendees should group up and buy beverages in rounds to minimize time spent in bar queue.
Attendees should settle their rounds in the group before the night is over.


## Misc
* commission should start shortly after 5pm
* commission should end or transfer to dinner plans no later than 8pm

## Glossary
* member - an individual who is invited to commissions
* attendee - an individual who intends on attneding a commissions
* commission location - the location at which the commission is held
* Øgård -> Hoegarden

[^1A]: Make use the rejseplanen API eventually
