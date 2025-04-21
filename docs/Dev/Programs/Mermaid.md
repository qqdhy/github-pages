Table of Content
- [[#Flowchart|Flowchart]]
	- [[#Flowchart#Directions|Directions]]
	- [[#Flowchart#Nodes|Nodes]]
	- [[#Flowchart#Links|Links]]
	- [[#Flowchart#Organization|Organization]]
	- [[#Flowchart#Multiple Nodes Links|Multiple Nodes Links]]
	- [[#Flowchart#Flowcharts|Flowcharts]]

[Tutorials | Mermaid](http://mermaid.js.org/config/Tutorials.html)
[About Mermaid | Mermaid](http://mermaid.js.org/intro/)
[Mermaid | Diagramming and charting tool](http://mermaid.js.org/#/)
[Diagram Syntax | Mermaid](http://mermaid.js.org/intro/syntax-reference.html)

## Flowchart

### Directions
```mermaid
flowchart TB
	A --> B
```

```mermaid
flowchart BT
	A --> B
```

```mermaid
flowchart LR
	A --> B
```

```mermaid
flowchart RL
	A --> B
```

### Nodes
```mermaid
graph TB
	id1[Hard edges]
	id2(Round edges)
	id3([Stadium])
	id4[[Subroutine]]
```

```mermaid
graph TB
	id6>Asymmetric]
	id7{Rhombus}
	id8{{Hexagon}}
```

```mermaid
flowchart TB
	id9[(Database)]
	id5((Circle))
	id6(((DoubleCircle)))
```

```mermaid
graph TB
	id9[/Parallelogram/]
	id10[\ParallelogramAlt\]
```

```mermaid
flowchart TB
	id11[/Trapezoid\]
	id12[\TrapezoidAlt/]
```

### Links
```mermaid
flowchart LR
	Normal --- N1 ---- N2 ----- N3
	NormalArrow --> NA1 ---> NA2 ----> NA3
	Thick === T1 ==== T2 ===== T3
	ThickArrow ==> TA1 ===> TA2 ====> TA3
	Dotted -.- D1 -..- D2 -...- D3
	DottedArrow -.- DA1 -..- DA2 -...- DA3
```

### Organization
```mermaid
flowchart TB
	A --> B
	A --> C
	A --> D
	B --> E
	B --> F
	C --> G
```

### Multiple Nodes Links
```mermaid
flowchart LR
	A --> B & C --> D
```

```mermaid
flowchart TB
	A & B --> C & D
```

### Flowcharts
```mermaid
flowchart LR
	A[Hard edge] --> |Link text| B(Round edge)
	B --> C{Decision}
	C -->|One| D[Result one]
	C -->|Two| E[Result two]
```

```mermaid
flowchart TB
	A(Start) --> B{Is it?}
	B --> |Yes| C[OK]
	C --> D[Rethink]
	D --> B
	B ----> |No| E(End)
```

## Sequence Diagram
```mermaid
sequenceDiagram
	autonumber
	actor Alice
	actor Bob
	Alice -> Bob: Solid
	Alice --> Bob: Dotted
	Alice ->> Bob: Solid arrow
	Alice -->> Bob: Dotted arrow
	Alice -x Bob: Solid cross
	Alice --x Bob: Dotted cross
	Alice -) Bob: Solid open arrow
	Alice --) Bob: Dotted open arrow
	Note over Alice, Bob: Lines and ends
```


