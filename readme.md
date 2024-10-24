# Movie ticket booking system idea
## Requirements
Design movie ticket booking system  
which can be sold to multiplex - multiple shows at different time spans  
and also option to books tickets show for normal people

## Use cases
### multiplex owners or cinema chains (B2B clients)
Common admin features like managing users, multiplex, cinema, seats plan, taxes, etc.  
Update new movies, show timings, prices, etc.  
Can reserve seats for special guests or VIPs, cancel bookings, etc.  
A dashboard to show statistics and reports (sales, booking rate, etc.).  
### Public customer (B2C clients)
Public website to browse movies, show timings, and book tickets online  
Select seats, make payment, receive eticket on email or SMS
### More options could be implemented (not in current scope)
discounts code input, pre-sell snacks and drinks, family packages, membership, etc.
## System overview
The system should has 2 user interfaces, one for multiplex owners and one for public customer.  
![System overview](./images/system%20overview.png)
## Admin microservices overview
For multiplex/cinema owners, the system should have the following features:
1. Admin user management - manage admin users, roles, permissions (Admin Service)
2. Multiplex management - manage multiplexes, cinema chains locations (Admin Service)
3. Cinema management - manage cinemas: halls/screens (Admin Service)
4. Show/Movie management - manage shows and movies, import/get movies info from external API (Show/Movie import/udate Service), update movies info, age restrictions, warnings, etc. (Show/Movie import/update Service)
5. Seat plan management - manage seats plan for each cinema (Admin Service)
6. Booking management - manage bookings for ticket, reserve seats, cancel bookings (Show/Movie browsing Service, ticket booking Service)
7. Dashboard - view statistics, manage reports (Admin Service)
### Admin microservices architecture
![Admin microservices architecture](./images/Admin%20microservices%20architecture.png)
## Public customer microservices overview
For public customers, the system should have the following features:
1. Movie browsing - browse movies, show timings, seats availability (Show/Movie browsing Service)
2. Ticket booking - select seats, make payment, receive eticket on email or SMS (ticket booking Service)
3. Payment - integrate with payment gateway for payment processing (Payment Service)
4. Notification - send email or SMS for booking confirmation, payment confirmation, etc.
5. User login - login, register, forgot password (Authentication Service)
6. User profile - manage user profile, view booking history (Website service)
### Public customer microservices architecture
![Public customer microservices architecture](./images/Public%20users%20microservices%20architecture.png)
## Full microservices architecture
![Full microservices architecture](./images/Full%20microservices%20architecture.png)
