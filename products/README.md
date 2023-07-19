# Products

In unTill Air, the 'Products' section follows a hierarchical structure where different levels are interconnected. At the foundation of this hierarchy is the 'Article' level, which serves as the fundamental block. As we move up the hierarchy, each level takes on a level of subordination until we reach the top level, which is the 'Category.' The 'Category' level includes all the other levels, forming a comprehensive and organized system for managing your restaurant's products.

***

```mermaid  fullWidth="false"

erDiagram
    Category ||--|{ Group  : "has"
    Group ||--|{ Department  : "has"
    Department ||--|{ Article  : "has"

```

```mermaid
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
