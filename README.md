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

