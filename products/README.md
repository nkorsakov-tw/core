# Products



```mermaid  fullWidth="true"
erDiagram
    Department ||--o{ Article : owns
    Department ||--o{ SpecialArticle : has
    SpecialArticle ||..|| Article: ref
    BO ||..o{ Article: "shows for department"
    POS ||..o{ Article: "shows for department"
    POS ||..o{ SpecialArticle: "shows for department"


```
