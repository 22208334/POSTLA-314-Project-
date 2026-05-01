# CMPE314 - Lab 4 Sequence Diagrams

## Part 1: Library Kiosk

![Library Kiosk](umlKiosk.png)

### Description
In the normal flow, the student places the book on the scanner, and the system scans and validates it using the library database. If the book is valid and returned on time, the system updates the inventory, sends a confirmation notification, and places the book back on the shelf. 

In an alternative flow, if the book is overdue, the system calculates a fine and requires payment before completing the return.
