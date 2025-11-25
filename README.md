# LOG FILE IMPLEMENTATION IN THE VFAT FILE SYSTEM OF LINUX

This project implements a **journaling mechanism for the VFAT file system** inside the **Linux Kernel Library (LKL)**. The goal is to extend the existing VFAT implementation so that every file-system modification is recorded in a structured journal. It was developed as part of the **MYY601 – Operating Systems** course at the  
**University of Ioannina**.

---

## TABLE OF CONTENTS
1. [Overview](#overview)  
2. [Features](#features)  
3. [Instructions](#instructions)  
4. [Implementation Details](#implementation-details)  
5. [Usage](#usage)  
6. [License](#license)  
7. [Contact](#contact)

---

## OVERVIEW

The project focuses on extending the **VFAT file system** inside the LKL environment by  
adding a **journaling subsystem**.  
The purpose of the journal is to:

- Log file-system operations  
- Provide structured records for debugging  
- Demonstrate how metadata consistency can be tracked  
- Capture each modification with timestamps and operation metadata  

The journaling feature is implemented without altering the semantics of VFAT,  
but by hooking into specific file-system operations and recording them.

---

## FEATURES

- **Journaling of File-System Operations**
  - Each VFAT modification produces a formatted log entry
  - Logs operation type, timestamp, and relevant metadata

- **Integration with LKL**
  - Works directly inside the Linux Kernel Library environment
  - No modifications to the native kernel needed

- **Extensible Journal Format**
  - Human-readable log entries  
  - Expandable structure for additional metadata

- **Minimal Overhead**
  - Journal writes kept lightweight and sequential

---

## INSTRUCTIONS

- **Objective:**  
  Extend the VFAT implementation in LKL to support journaling of file-system changes.

- **Required Tasks:**  
  - Create a **journal structure and API**  
  - Capture VFAT operations (create, delete, write, etc.)  
  - Append entries to the journal log file  
  - Ensure journal format matches the specification given in the exercise  
  - Implement and test using LKL’s user-space tools

- **Expected Output:**  
  A journal file containing correctly formatted log entries, each describing  
  a file-system modification.

---

## IMPLEMENTATION DETAILS

- **Journal Structure**
  - A dedicated log file is created for the journal
  - Each entry contains:
    - Operation type  
    - Target path  
    - Timestamps  
    - Additional metadata required by the exercise  

- **Integration Points**
  - Hooks inserted at VFAT operation handlers  
  - Operations such as:
    - File creation  
    - File deletion  
    - Directory creation  
    - Write operations  

- **Logging Logic**
  - Synchronous append operations  
  - Ensures sequential and readable records  
  - Minimal kernel-side overhead

- **Build Environment**
  - Based on LKL’s build system  
  - VFAT-related source files extended with journaling calls

---

## USAGE

1. **Rebuild LKL** with the modified VFAT source files  
2. **Run the LKL user-space environment**  
3. Perform file operations (create, write, delete, etc.) inside the mounted VFAT filesystem  
4. Inspect the **generated journal log** to verify recorded entries

---

## LICENSE

This project was developed as part of the  
**MYY601 – Operating Systems** course at the University of Ioannina.

Final implementation by the project creators.

---

## CONTACT

**Christos Gkovaris**  
University of Ioannina – Computer Science and Engineering  
GitHub: https://github.com/ChristosGkovaris

**Maria Spanou**  
University of Ioannina – Computer Science and Engineering  
GitHub: https://github.com/SpanouMaria
