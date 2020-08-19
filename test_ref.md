---
title: STQL reference
kind: Documentation
aliases:
  - /reference/stql_reference/
listorder: 1
---

# STQL (StackState Query Language) reference guide

The built-in StackState Query Language (STQL) can be used to run advanced queries in the StackState Topology and Analytics environments.
* **Topology:** Use STQL to build [advanced topology filters]() that zoom in on specific areas of your topology or highlight components and their root cause.
* **Analytics:** Combine STQL with [scripting]() to create powerful queries that access the entire 4T data model.

STQL queries consist of component filters and STQL functions. The query output is a component, or set of components, from the complete topology.

# Component filters

Component filters are used in two ways in STQL:
* Define the set of components to be included in the query output.
* Specify the set of components to be handled by an in-built STQL function.

The basic filters described below can be combined using boolean operators to achieve complex selections of components. Note that boolean operators will be executed in the standard order: NOT, OR, AND. You can change the order of operations by grouping sections of a query with parentheses (...).

## Basic filters

| Filter | Default | Allowed values | Description |
| :--- | :--- | :--- | :--- |
| `domain` | all | ... | ... |
| `environment` | all | ... | ... |
| `healthstate` | all | DEVIATING, CRITICAL | Components with the named healthstate |
| `label` | all | ... | Components with the named labels |
| `layer` | all | ... | Components in the named layer |
| `name` | all | ... | ... |
| `type` | all | ... | ... |

### Example usage

```
# Select all components with name serviceB
name = "serviceB"

# Select all components in the application** layer:
layer = "application"

# Select all components with name of either appA or appB that do not have a label bck
name in ("appA","appB") NOT label = "bck"
```


| STQL | Description |
| :--- | :--- |
| `name = "serviceB"` | Select all components with name **serviceB** |
| `layer = "application"` | Select all components in the **application** layer |
| `name in ("appA","appB") NOT label = "bck"` | Select all components with name of either **appA** or **appB** that do not have a label **bck** |

Select all components with name **serviceB**
* `name = "serviceB"`
Select all components in the **application** layer:
* `layer = "application"`
Select all components with name of either **appA** or **appB** that do not have a label **bck**
* `name in ("appA","appB") NOT label = "bck"`

