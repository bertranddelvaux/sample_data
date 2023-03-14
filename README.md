# sample_data

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```


For example this is a Block level $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$ formula, and this is an inline Level $x = {-b \pm \sqrt{b^2-4ac} \over 2a}$ formula.

\\[ \frac{1}{\Bigl(\sqrt{\phi \sqrt{5}}-\phi\Bigr) e^{\frac25 \pi}} =
1+\frac{e^{-2\pi}} {1+\frac{e^{-4\pi}} {1+\frac{e^{-6\pi}}
{1+\frac{e^{-8\pi}} {1+\ldots} } } } \\]

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column


```plantuml
@startuml

User -> (Start)
User --> (Use the application) : A small label

:Main Admin: ---> (Use the application) : This is\nyet another\nlabel

@enduml
```

```mermaid
graph LR
    id1[(fa:fa-database raw data)] -->|pre-processing| B(data for modelling)
    B --> C{fa:fa-chart-bar models}
    C --> D[Linear Regression]
    C --> E[Random Forest]
    C --> F[KNN]
    D --> G[ensemble]
    E --> G
    F --> G
    G --> id2[(predictions)]
```

```mermaid
flowchart TB
    subgraph Legend
      direction LR
      start1[ ] ----|protocol schema definition| stop1[ ]
      style start1 height:0px;
      style stop1 height:0px;
      start2[ ] --->|protoBuf message| stop2[ ]
      style start2 height:0px;
      style stop2 height:0px; 
      start3[ ] -..->|meta data| stop3[ ]
      style start3 height:0px;
      style stop3 height:0px; 
    end
    A --- B & I
    E --> F
    F --> G
    a -.->|GATT| F
    subgraph GitHub
        A{{.proto}}
    end
    subgraph Device
        B{{.proto}}
        C[[Sensors]]
        D{Serializer}
        E((ProtoBuf))
        a[ ]
        B -.-> D
        B -.->|<protocol_id>\n<hash_commit>| a
        C --> D
        D --> E
    end
    subgraph Application
        F((ProtoBuf))
        F[ ] -.->|<account_id>\n<user_id>\n<recording_mode>\n<hash_commit>\n<protocol_id>| F
    end
    subgraph Backend
        subgraph HotBucket
            G((ProtoBuf))
        end
        subgraph CloudFunction
            I{{.proto}}
        end
        J{Deserializer}
        K[(Storage)]
        G -.->|<account_id>\n<user_id>\n<recording_mode>| K
        G --> J
        I -.-> J
        J ---> K
        G -.->|\n<hash_commit>\n<protocol_id>| CloudFunction
    end
    style GitHub fill:#DEFCDBFF, stroke:white;
    style Device fill:#DBFCF7FF, stroke:white; 
    style Application fill:#DBECFCFF, stroke:white;
    style Backend fill:#DEDBFCFF, stroke:white;
    style CloudFunction fill:#F5DBFCFF, stroke:white;
    style HotBucket fill:#F5DBFCFF, stroke:white;
    style Legend fill:#FFFFFF77, stroke:white;
    style A fill:#D085FFFF;
    style B fill:#D085FFFF;
    style I fill:#D085FFFF;
    linkStyle 0 stroke:magenta;
    linkStyle 1 stroke:blue;
    linkStyle 3 stroke:magenta;
    linkStyle 4 stroke:magenta;
    linkStyle 5 stroke:blue;
    linkStyle 6 stroke:blue;
    linkStyle 14 stroke:blue;
    style E fill:#76C3FFFF;
    style F fill:#76C3FFFF;
    style G fill:#76C3FFFF;
    style a height:0px;
```

