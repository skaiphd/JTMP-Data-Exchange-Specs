# New Case Initiation Exchange

A Courts' Case Management (CMS)) will publish a a Case Initiation message each time a Clerk creates a new Criminal case (other case types?). This data exchange serves two purposes: to provide case details and a court case number to parties that need to track or contribute to case processing; and to correlate a court case with a preceeding event sent by another publishing system, for example a Booking message published by the jail management system (JMS). 

The publisher may be the CMS of any court jurisdiction - Criminal, Juvenile, or Municipal & Traffic. 

## Preceding Exchange: 

Booking

## Triggering Event:

1. Magistrate Court binds a new arrest over to Criminal court
2. Court clerk creates a new case, assigning a criminal case ID number as well as a  judge and courtroom. 
Note: this process of assigning new criminal cases was known as Allotment. This transactional data exchange replaces the Allotment List, in conveying new case information to all interested parties. 

## Subsequent Event:
Proposed Motions and Orders filed to the Clerk by case parties

## Real-World Effects: 

The purpose of this data exchange is to enable partner justice systems to either set up a new case or to associate court proceedings with a preceeding event, such as a jail booking. This exchange should be triggered as soon as a new court case is created in order to keep partners like the prosecutor and public defender apprised and enable them to take the next actions in court in a timely manner. 

This exchange is also intended to improve efficiency and accuracy. Subscriber systems should use the incoming data in this XML payload to create a new Matter or Case (depending on the system's terminology) in time to review details and prepare filings for court. Improvements in data accuracy and completeness result, since data will populate automatically in the Subscriber systems. Reduction of re-keying of information saves staff time and reduces or elimiates errors.  The errors in re-keying obscure identifying numbers like SSN or court case ID reduce the types of errors that lead to case delays and ill-informed decision-making. 

## Data Requirements:

XML Schemas - coming soon

### Key data elements include:
- Arrest number (enabling the JMS to correlate a new case to a previous Booking or Charge Screening. 
- Court Case ID
- Case Initiation (new criminal case established, Court publishes Case Number and Filed Charges)​
- Created Date (court clerk's staff will determine if this is a machine-generated date-time stamp, or the date of the judicial officer's approval)
- Judicial Official (the Judge or Magistrate who approved/signed the Order)
- Current charges (either arrest charges or filed charges if the DA has filed a Screening Action Form). 
- SCN-Sequence number to correlate each Charge to the value originally assigned in the State's AFIS and CCH. 

## Artifacts:

Mapping Spreadsheet - coming soon

**Class Diagram:** - coming soon


Sample XML File - coming soon


