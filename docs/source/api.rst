# Documentation for Orchestrator


## Using Mermaid Diagram

Create .md file and draw diagram with mermaid inside Markdown fenced code.  
Fenced code means code covered with ```. And after first three apostrophe, you can specify syntax.  
Checkout this file as raw format.  

In vscode, you can download extension "Markdown Preview Mermaid Support" to see live preview of md file.  
You can refer mermaid syntax on following link [mermaid docs](https://mermaid.js.org/intro/).

You can add mermaid diagram to confluence wiki with draw.io macro.  
Click Plus button at menu bar, and Advanced > Mermaid.


```mermaid
---
title: Sample State Diagram
---
stateDiagram-v2
    [*] --> Still : Start watching
    Still --> [*] : End watching

    Still --> Moving : Trigger
    Moving --> Still : Time passes
    Moving --> Crash : Obstacle
    Crash --> [*] : End watching
```
```
---
title: Sample State Diagram
---
stateDiagram-v2
    [*] --> Still : Start watching
    Still --> [*] : End watching

    Still --> Moving : Trigger
    Moving --> Still : Time passes
    Moving --> Crash : Obstacle
    Crash --> [*] : End watching
```
```mermaid
---
title: Sample ClassDiagram
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```
```
---
title: Sample ClassDiagram
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

```mermaid
---
title: Sample Sequence Diagram
---
sequenceDiagram
    actor A as Alice
    box Box
    actor John
    participant Sam
    end
    A->>John: Hello John, how are you?
    John-->>Sam : Alice talked to me!
    John-->>A: Great!
    A-)John: See you later!
```
```
---
title: Sample Sequence Diagram
---
sequenceDiagram
    actor A as Alice
    box Box
    actor John
    participant Sam
    end
    A->>John: Hello John, how are you?
    John-->>Sam : Alice talked to me!
    John-->>A: Great!
    A-)John: See you later!
```


```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
    Functionality added                 :milestone, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```
```
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d
    Functionality added                 :milestone, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```
