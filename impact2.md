# Impact Direction for Sales

There are multiple ways to think about how to apporach this.

## Agency Workflow 2

```mermaid
flowchart TD
    ApplyCriteria{"Apply\nImpact\nCriteria"}
    ApplyCriteria-->Proceed;
    ApplyCriteria-->Collaborate;
    ApplyCriteria-->NotAligned["Not Aligned"];
    Collaborate-->SalesSubmits["Sales submit opportunity"];
    SalesSubmits-->ImpactResponds["Impact committee acknowledges"];
    ImpactResponds-->Decision{"Impact\nCommittee\ndecison"};
    Decision-->Proceed;
    Decision-->NotAligned;


  NotAligned-->SalesSubmitsImpactRed["Sales determines impact opportunity"];
  SalesSubmitsImpactRed-->ImpactRespondsRed["Impact committee acknowledges"];
  ImpactRespondsRed-->ImpactDiscussesRed{"Impact\nCommittee\ndecison"};
  ImpactDiscussesRed-->InvolveGovernanceRed[Escalate to Impact\nGovernance Committee]
  ImpactDiscussesRed-->DecisionRed{"Decison"};
  InvolveGovernanceRed-->DecisionRed;
  DecisionRed-->Proceed;
  DecisionRed-->NotAligned;

style Proceed fill:lightgreen
style Collaborate fill:yellow
style NotAligned fill:red

style ApplyCriteria fill:pink;
style SalesSubmits fill:pink;
style SalesSubmitsImpactRed fill:pink;

style InvolveGovernanceRed fill:darkblue,color:white;
```

## Values workflow 2

```mermaid
graph TD
   DITAP-->Tier1;
   Accessibility[[Accessibility Focus]]-->Tier1;
   Sustainability[[Environmental Sustainability Focus]]-->Tier1;
   Open[[Open Government Focus]]-->Tier1;
   Tier1[[T1 Values aligned]]-->Yes;
   Tier2[[T2 Organization aligned]]-->Yes
   Tier3[[T3 Smaller]]-->Maybe
```

## Values workflow 3

```mermaid
graph TD
   DITAP-->Tier1;
   Accessibility[[Accessibility Focus]]-->Tier1;
   Sustainability[[Environmental Sustainability Focus]]-->Tier1;
   Open[[Open Government Focus]]-->Tier1;
   Tier1[[T1 Values aligned]]-->Yes;
   Tier2[[T2 Organization aligned]]-->Yes
   Tier3[[T3 Smaller]]-->Maybe
```
