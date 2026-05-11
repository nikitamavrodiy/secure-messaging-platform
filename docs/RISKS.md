| ID | Risk                                        | Impact | Simple Fix (Mitigation)                                  |
| -- | ------------------------------------------- | ------ | -------------------------------------------------------- |
| R1 | Messages may not be delivered in real time  | High   | Store messages first and ensure proper delivery handling |
| R2 | Login/security issues                       | High   | Use proper authentication checks and session validation  |
| R3 | Messages may not be saved correctly         | Medium | Save messages before confirming delivery                 |
| R4 | System may become slow with many users      | Medium | Keep design simple and avoid heavy processing            |
| R5 | System parts may not work together properly | Medium | Integrate features step-by-step and test each part       |
