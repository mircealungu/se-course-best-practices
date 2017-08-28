This document lists all deliverables and factors that contribute to the final grade.

## Feedback
**Each iteration** (every two weeks) the team delivers:
- [Pull request to master](/Git%20Workflow.md).
- [Requirements document](/example-documents/README.md#requirements-document).
- [Architecture document](/example-documents/README.md#architecture-document).
- Log of recorded working hours.

The Teaching Assistant delivers feedback on these deliverables, 
such that the team knows if they are on the right track.

## Intermediate Grade
**Half-way** and at the **end** of the course, we determine a student's intermediate grade G<sub>i</sub> (for i=0,1).

Del<sub>i</sub> = (CQ + (AD + RD + PR + FU) / 2) / 3

Pro<sub>i</sub> = 0.2 + (SP + TP + CP) / 30

Per<sub>i</sub> = 0.2 + PC / 10

<P align=center>
G<sub>i</sub> = MIN(10, Del<sub>i</sub> * Pro<sub>i</sub> * Per<sub>i</sub>)
</P>

Where the factors are:
- **CQ** - Code Quality
- **FU** - Functionality
- **RD** - Requirements Document
- **AD** - Architecture Document
- **PR** - [Presentation](/example-documents/README.md#presentation)
- Team Professionalism: 
  - **SP** - Wrt. Staff
  - **TP** - [Wrt. Team](/evaluation/Peer%20Evaluation.md)
  - **CP** - [Wrt. Customer](/evaluation/Client%20Evaluation.md)
- **PC** - [Personal Contribution](/evaluation/Peer%20Evaluation.md)

## Final Grade
The two intermediate grades are used to calculate the final grade:
<P align=center>
G<sub>final</sub> = (G<sub>0</sub> + G<sub>1</sub>) / 2
</P>
