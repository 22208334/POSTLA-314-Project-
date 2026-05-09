# CMPE314 - Lab 2 Gantt Chart

## Project Title
POSTLA Project

## Team Members
- Deniz Onat Bayer
- Umut Sevinç
- Muhammet Salih Erol
- Melik Koçhan

## Project Description
This project focuses on project planning and scheduling for a software engineering project. The Gantt chart demonstrates task durations, dependencies, milestones, and resource allocation among team members.

## Gantt Chart

![Gantt Chart](ganttchart.png)




## # CMPE314 - Lab 3 Online Bookstore Use Case Diagram

The Online Bookstore use case diagram represents the main interactions between users and the bookstore system. Customers can browse books, search for books, and view book details. Registered customers can log in, add books to their cart, and place orders. The checkout process includes payment processing through an external payment gateway. Administrators manage books and update payment or order status within the system.

### Actors
- Customer: Browses, searches, and views book information.
- Registered Customer: Logs in, adds books to cart, and places orders.
- Admin: Manages books and updates order/payment status.
- Payment Gateway: Handles payment processing.

### Main Use Cases
- Browse Book
- Search Book
- View Book Details
- Login
- Add to Cart
- Place Order
- Checkout
- Process Payments
- Manage Books
- Update Payment Status

- ![Online Bookstore Use Case Diagram](OnlineBookStore.png)



## POSTLA Use Case Diagram

The POSTLA use case diagram represents the core functionalities of the POSTLA web-based post scheduler system. Users and creators can register, log in, manage their profiles, create draft posts, upload media, schedule posts, and view their calendar dashboard. Student clubs and community managers can use the platform to organize scheduled posts and manage their content plans. The system administrator is responsible for managing users, maintaining the database, and monitoring server health. The publishing engine checks scheduled times and publishes posts automatically through the connected social media API.

### Actors
- User / Creator: Creates, edits, schedules, and manages posts.
- Student Club / Community Manager: Plans and manages scheduled announcements or community posts.
- System Administrator: Manages users, database maintenance, and server monitoring.
- Publishing Engine / Cron Job: Automatically checks scheduled posts and triggers publishing.
- Social Media API: External service used for publishing scheduled posts.

### Main Use Cases
- Register
- Login
- Manage Profile
- Create Draft Post
- Upload Media
- Schedule Post
- Prevent Scheduling Conflict
- View Calendar Dashboard
- View Scheduled Posts
- Publish Scheduled Post
- Check Scheduled Time
- Manage Users
- Maintain Database
- Monitor Server Health

- ![Online Bookstore Use Case Diagram](POSTLADiagrampng)

# CMPE314 - Lab 4 Sequence Diagrams

## Part 1: Library Kiosk

![Library Kiosk](umlKiosk.png)

### Description
In the normal flow, the student places the book on the scanner, and the system scans and validates it using the library database. If the book is valid and returned on time, the system updates the inventory, sends a confirmation notification, and places the book back on the shelf. 

In an alternative flow, if the book is overdue, the system calculates a fine and requires payment before completing the return.

## Part 2: POSTLA Project

![POSTLA Diagram](umlPOSTLA.png)

### Description
In the normal flow, the content creator creates a post and schedules it using the dashboard. The system validates the content, saves it in the database with a scheduled status, and confirms the scheduling.

In an alternative flow, the scheduler engine periodically checks for posts that are ready to be published. When a post is due, it is sent to the social media API, and upon successful publishing, the system updates the post status, starts analytics tracking, and sends a notification to the user indicating that the post is live.





# CMPE314 – Lab 5 Activity Diagrams

## Part 1 – Library Kiosk Return Book Activity Diagram

![Library Kiosk Activity Diagram](LibraryKiosk-Return%20Book%20Activity%20Diagram.png)

### Description
This activity diagram represents the workflow of returning a book through a library kiosk system. The process starts when a student places a book on the scanner, and the system validates the book using the library database. If the book is invalid, the system displays an error and rejects the return process.

If the book is valid, the system checks whether the book is overdue. For overdue books, the system calculates a fine and asks the student to complete the payment before continuing. Once the return is accepted, the system performs several parallel activities, including updating the inventory, sending a return confirmation notification, and placing the book back on the shelf. Finally, the return process is completed successfully.

---

## Part 2 – POSTLA Schedule Post Activity Diagram

![POSTLA Activity Diagram](postla_schedule_post_activity_diagram.png)

### Description
This activity diagram represents the workflow of scheduling a social media post in the POSTLA platform. The process begins when the user logs into the system and opens the scheduling dashboard. The user can create or select a draft post, enter post details, optionally upload media files, and choose a publishing date and time.

The system validates the selected time and checks for scheduling conflicts. If the selected time is invalid or conflicts with another scheduled post, the system suggests corrections and returns the user to the scheduling step. Once the post is successfully scheduled, the system performs parallel activities such as storing the post in the database, displaying it on the calendar dashboard, and creating a cron publishing job. Finally, the post is automatically published at the scheduled time, and the user receives a notification confirming the publishing process.
