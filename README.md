## Cloud Firestore (Firebase)
Firestore is a NoSQL document database provided by Google Firebase.

# What is a NoSQL Database?
A NoSQL database stores data not in the form of tables (rows and columns) like SQL databases. Instead, it stores data in flexible formats like documents (JSON-like). Firestore organizes data as: Collections → Documents → Fields.

NoSQL is useful for modern applications because it is scalable, fast, and flexible.

Schema Design (Collection + Fields)
Collection Created: evidence

Documents:
Each document represents one evidence record (example: case_001, case_002).

Fields Used:
Field Name	Data Type	Meaning
clue_type	string	Type of evidence (Fingerprint/DNA/CCTV etc.)
is_verified	boolean	Whether the clue is verified (true or false)
timestamp	timestamp	Time when the record was created/added
Additional test fields used:

location (string)
officer (string)
notes (string)
Data Entry
Two documents were added manually inside the collection:

Example Documents:
case_001

clue_type: "Fingerprint"
is_verified: true
timestamp: Firestore Timestamp
case_002

clue_type: "DNA"
is_verified: false
timestamp: Firestore Timestamp
CRUD Operations (Frontend Implementation)
A frontend webpage was created using HTML + JavaScript Firebase SDK to perform CRUD on Firestore.

CRUD = Create, Read, Update, Delete

Implemented CRUD Features:

 Create: Add new evidence record into /evidence collection using a document ID
 Read: Display all evidence records from Firestore in a table
 Update: Edit clue_type and is_verified values in Firestore
 Delete: Remove an evidence record from Firestore
