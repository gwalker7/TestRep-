# TestRep-


```mermaid
flowchart TD
A --> B
B --> C

```mermaid
%%{init: { 'gitGraph': { 'mainBranchName': 'develop'}} }%%
gitGraph
  commit
  commit
  
  branch release/2023.1.0
  commit
  checkout release/2023.1.0
  
  branch dev1/DDAI-123-some-bugfix
  checkout dev1/DDAI-123-some-bugfix
  commit
  checkout release/2023.1.0
  merge dev1/DDAI-123-some-bugfix
  
  branch dev1/DDAI-124-another-bugfix
  checkout dev1/DDAI-124-another-bugfix
  commit
  commit
  commit
  checkout release/2023.1.0
  merge dev1/DDAI-124-another-bugfix

  checkout develop
  commit
  commit
  commit
  commit
  commit
  commit

  checkout release/2023.1.0
  branch dev2/DDAI-125-one-more-bug
  checkout dev2/DDAI-125-one-more-bug
  commit
  commit
  checkout release/2023.1.0
  merge dev2/DDAI-125-one-more-bug

  checkout develop
  merge release/2023.1.0
  commit
  commit
  commit
  commit

  branch release/2023.2.0
  commit
  checkout release/2023.2.0
  
  branch dev1/DDAI-200-some-bugfix
  checkout dev1/DDAI-200-some-bugfix
  commit
  checkout release/2023.2.0
  merge dev1/DDAI-200-some-bugfix
  
  checkout develop
  merge release/2023.2.0
