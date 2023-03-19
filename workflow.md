# graph
Simple accessibility workflow


## Workflow 1

```mermaid
graph TD

      accTitle: Workflow 1
      accDescr {  Workflow   }

    Start-->CheckoutCode;
    CheckoutCode-->SetupDDev;
    SetupDDev-->BuildSite;
    SetupDDev-->ImportDatabase;
    BuildSite-->AccessibilityTests;
    ImportDatabase-->AccessibilityTests;
    AccessibilityTests-->End;
```


## Workflow 2

```mermaid
graph TD

      accTitle: Workflow 2
      accDescr {  Workflow   }

    Start-->CheckoutCode;
    CheckoutCode-->SetupDDev;
    SetupDDev-->BuildSite;
    SetupDDev-->ImportDatabase;
    BuildSite-->AccessibilityTests;
    ImportDatabase-->AccessibilityTests;
    AccessibilityTests-->CypressTests;
    CypressTests-->SonarQubeScan;
    SonarQubeScan-->PushCodeToAcquia;
    PushCodeToAcquia-->End;
```


## Workflow 3

```mermaid
graph TD

      accTitle: Workflow 3
      accDescr {  Workflow   }

    Start-->CheckoutCode;
    CheckoutCode-->SetupDDev[Setup DDev];
    SetupDDev-->BuildSite;
    SetupDDev-->ImportDatabase;
    BuildSite-->AccessibilityTests;
    ImportDatabase-->AccessibilityTests{Accessibility Tests};
    AccessibilityTests --> |No Errors| CypressTests;
    AccessibilityTests --> |Errors| CommitFails[Commit Fails]
    CypressTests-->SonarQubeScan;
    SonarQubeScan-->PushCodeToAcquia;
    PushCodeToAcquia-->End;
```

