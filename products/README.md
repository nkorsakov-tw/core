# Products

In unTill Air, the 'Products' section follows a hierarchical structure where different levels are interconnected. At the foundation of this hierarchy is the 'Article' level, which serves as the fundamental block. As we move up the hierarchy, each level takes on a level of subordination until we reach the top level, which is the 'Category.' The 'Category' level includes all the other levels, forming a comprehensive and organized system for managing your restaurant's products.

***

```mermaid  fullWidth="false"

erDiagram
    Category ||--|{ Group  : "has"
    Group ||--|{ Department  : "has"
    Department ||--|{ Article  : "has"

```

```mermaid  fullWidth="false"
flowchart LR
  Category:::G
  subgraph Category
    direction LR
    Group1:::G
    subgraph Group1
        Dep1.1:::G
        subgraph Dep1.1
            direction LR
            subgraph Art1.1.1
            end
            subgraph Art1.1.2
            end
        end
        Dep1.2:::G
        subgraph Dep1.2
            direction LR
            subgraph Art1.2.1
            end
            subgraph Art1.2.2
            end        
        end
    end
    Group2:::G
    subgraph Group2
        Dep2.1:::G
        subgraph Dep2.1
            direction LR
            subgraph Art2.1.1
            end
            subgraph Art2.1.2
            end
        end
        Dep2.2:::G
        subgraph Dep2.2
            direction LR
            subgraph Art2.2.1
            end
            subgraph Art2.2.2
            end        
        end
    end
  end

  classDef G fill:#FFFFFF,stroke:#000000, stroke-width:1px, stroke-dasharray: 5 5  

```





```mermaid
graph TD
  %% Entities =================================

  Categories:::S
  subgraph Categories
    Category1[Food]:::C
    Category2[Drinks]:::C
  end

  Groups:::S
  subgraph Groups
    Group1.1[Starters]:::G
    Group1.2[Main Dishes]:::G
    Group1.3[Deserts]:::G
    Group2.1[Alcohol]:::G
    Group2.2[Non-Alcohol]:::G
  end

  Departments:::S
  subgraph Departments
    Department1.1.1[Cold Starters]:::D
    Department1.1.2[Salads]:::D
    Department2.1.1[Beers]:::D
    Department2.1.2[Vines]:::D
    Department2.1.3[Long Drinks]:::D
    Department2.2.1[Cold Drinks]:::D
    Department2.2.2[Coctails]:::D
    Department2.2.3[Hot Drinks]:::D
  end
  
  Articles:::S
  subgraph Articles
    Article1.1.1.1(Gaspacho):::A
    Article1.1.1.2(Cold Salmon):::A
    Article2.2.1.1(Sparkling Water):::A
    Article2.2.1.2(Orange Juice):::A
  end  


  %% Relations =================================
  
  Category1 --- Group1.1
    Group1.1 --- Department1.1.1
       Department1.1.1 --- Article1.1.1.1
       Department1.1.1 --- Article1.1.1.2
    Group1.1 --- Department1.1.2
  Category1 --- Group1.2
  Category1 --- Group1.3

  Category2 --- Group2.1
    Group2.1 --- Department2.1.1
    Group2.1 --- Department2.1.2
    Group2.1 --- Department2.1.3
  Category2 --- Group2.2
    Group2.2 --- Department2.2.1
        Department2.2.1 --- Article2.2.1.1
        Department2.2.1 --- Article2.2.1.2
    Group2.2 --- Department2.2.2
    Group2.2 --- Department2.2.3

  classDef S fill:#FFFFFF,stroke:#000000, stroke-width:1px, stroke-dasharray: 5 5
  classDef C fill:#FFFFB5
  classDef G fill:#C9E7B7
  classDef D fill:#B5FFFF
  classDef A fill:#F5FFFF
```
