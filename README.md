For private documents

<!-- Headers -->
# Headers
# This is an H1
## This is an H2
### This is an H3
#### This is an H4
##### This is an H5
###### This is an H6 

<!-- Blockquotes -->
# Blockquotes
As Kanye West said:

> We're living the future so
> the present is our past.

<!-- Lists -->
# Lists
* リスト1
    * リスト1-2  
* リスト2  

<!-- Decimal -->
#### Ordered List
1. リスト1-1
    2. リスト1-2
2. リスト2  

<!-- Checkbox -->
- [ ] リスト1
- [x] リスト2

<!-- Links -->
# Links
<https://github.com/takaoyuya/doc>
[Repositry](https://github.com/takaoyuya/doc)

<!-- Links -->
# Images
![Finder](/images/preview-scroll-sync.gif)

<!-- Emphasis -->
# Emphasis
*Emphasis*
**Emphasis**
***Emphasis***
==marked==

# Abbreviation
*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.

<!-- strike-through -->
# Strike-Through
~~打ち消し~~

<!-- code -->
# Inline code
I think you should use an
`<addr>` element here instead.

<!-- code -->
```
function add(x, y) {
  return x + y;
}
```

# Emoji
:white_check_mark: Dos
:x: Don'ts
:warning:	
:no_entry_sign:	
:bangbang:	
:bomb:

# Alerts
> [!NOTE]
 Highlights information that users should take into account, even when skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.

<!-- Tables -->
# Tables
| Left align | Right align | Center align |
| :--------- | ----------: | :----------: |
| This       |        This |     This     |
| column     |      column |    column    |
| will       |        will |     will     |
| be         |          be |      be      |
| left       |       right |    center    |
| aligned    |     aligned |   aligned    |

<!-- Diagrams -->
# Diagrams
### Sequence diagram
<script>
  mermaid.initialize({ sequence: { showSequenceNumbers: true } });
</script>

```mermaid {code_block=true}
---
title: sequenceDiagram example
---
sequenceDiagram
autonumber
actor Alice
activate Alice
Alice->>Charles: Hello Charles, how are you(sync)
loop HealthCheck
    Charles->>Charles: Fight against hypochondria
end
Note right of Charles: Rational thoughts!
Charles--xAlice: Great!(Error)
Charles-)Bob: How about you?(async)
alt is sick
    Bob->>Charles: Not so good :(
else is well
    Bob->>Charles: Feeling fresh like a daisy
end
opt Extra response
    Bob->>Charles: Thanks for asking
end

%% this is a comment
par Alice to Bob
    Alice->>Bob: Hello guys!
and Alice to Charles
    Alice->>Charles: Hello guys!
end
Bob-->>Alice: Hi Alice!
Charles-->>Alice: Hi Alice!
deactivate Alice

```

### Class diagram
```mermaid {code_block=true}
---
title: classDiagram example
---
classDiagram
Class01 <|-- AveryLongClass : Cool
<<Interface>> Class01
Class09 --> C2 : Where am I?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla

Customer "1" --> "*" Ticket
Student "1" --> "1..*" Course

namespace BaseShapes {
    class Triangle
    class Rectangle {
      double width
      double height
    }
}
```

### State diagram
```mermaid {code_block=true}
---
title: stateDiagram example
---
stateDiagram-v2
classDef notMoving fill:white
classDef badBadEvent fill:#f00,color:white,font-weight:bold,stroke-width:2px,stroke:yellow
[*] --> Still:::notMoving
Still --> [*]
Still --> Moving
state if_state <<choice>>
Moving --> Still: cancel
Moving --> if_state
if_state --> [*]: OK
if_state --> Crash : NG
Crash:::badBadEvent --> [*]

```

### gantt chart
```mermaid {code_block=true}
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Milestone
        KickOff : done, b, 2024-06-01, 0d
        UAT :crit, b, 2024-07-13, 5d
        Rehearsal : milestone, b, 2024-07-26, 0d
        Release : milestone, b, 2024-08-01, 0d
    section Section
        A task          :done, 2024-06-01, 5d
        B task          :active, 2024-06-07, 30d
        C task    : ,2024-06-17, 20d
    section Another
        D Task :2024-06-12, 12d
        E Task    :24d
```


### quadrant chart
```mermaid {code_block=true}
---
title: quadrantChart example
---
%%{init: {"quadrantChart": {"chartWidth": 400, "chartHeight": 400}, "themeVariables": {"quadrant1TextFill": "#ff0000"} }}%%
quadrantChart
  x-axis Urgent --> Not Urgent
  y-axis Not Important --> "Important ❤"
  quadrant-1 Plan
  quadrant-2 Do
  quadrant-3 Delegate
  quadrant-4 Delete
```

### gitGraph chart
```mermaid {code_block=true}
---
title: gitGraph example
---
%%{init: { 'logLevel': 'debug', 'theme': 'forest' } }%%
      gitGraph
        commit
        branch hotfix
        checkout hotfix
        commit
        branch develop
        checkout develop
        commit id:"ash" tag:"abc"
        branch featureB
        checkout featureB
        commit type:HIGHLIGHT
        checkout main
        checkout hotfix
        commit type:NORMAL
        checkout develop
        commit type:REVERSE
        checkout featureB
        commit
        checkout main
        merge hotfix
        checkout featureB
        commit
        checkout develop
        branch featureA
        commit
        checkout develop
        merge hotfix
        checkout featureA
        commit
        checkout featureB
        commit
        checkout develop
        merge featureA
        branch release
        checkout release
        commit
        checkout main
        commit
        checkout release
        merge main
        checkout develop
        merge release

```


# Footnotes
Content [^1]
[^1]: Hi! This is a footnote

<!-- Extended syntax -->
# Extended syntax
30^th^
H~2~O

### Customize CSS
The style.less file will open, and you can override existing style

### References
[Markdown Preview Enhanced](https://shd101wyy.github.io/markdown-preview-enhanced/#/code-chunk)

[Mermaid](https://github.com/mermaid-js/mermaid)

[GitHub フォーマットの構文](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[絵文字チート シート(GitHub)](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)