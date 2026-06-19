 Netflix Database System

A relational database system inspired by Netflix, built as part of  Database Systems final project.

  Description
This project simulates a Netflix-like relational database that manages users, profiles,
subscriptions, payments, content, and watch history using proper relational model design.

 Features
-  User & Profile management
-  Content catalog (Movies & Series)
-  Subscription & Payment tracking
-  Device management
-  Genre & Language categorization
-  Review & Rating system
-  Watch History tracking


 Database Tables (15 Tables)

### Strong Entities
| Table | Description |
|-------|-------------|
| `USER` | Stores user ID, name, email, password, date joined |
| `PROFILE` | Stores profile name, age restriction, language, linked to USER |
| `SUBSCRIPTION` | Stores plan type (Basic/Standard/Premium), price, status |
| `PAYMENT` | Stores amount, date, method (Card/Debit/Prepaid), status |
| `DEVICE` | Stores device type (Mobile/TV/Laptop/Tablet), OS, linked to USER |
| `CONTENT` | Parent entity storing title, release year, type (Movie/Series), rating |
| `EPISODE` | Stores episode number, season, title, duration, linked to SERIES |
| `GENRE` | Stores genre names |
| `LANGUAGE` | Stores language names and codes |
| `REVIEW` | Stores star ratings (1-5), review date, linked to PROFILE & CONTENT |

### Child Entities (IsA Relationship)
| Table | Description |
|-------|-------------|
| `MOVIE` | Inherits from CONTENT; stores movie duration & box office |
| `SERIES` | Inherits from CONTENT; stores total seasons |

### Bridge Tables
| Table | Description |
|-------|-------------|
| `WATCH_HISTORY` | Links PROFILE ↔ CONTENT; tracks watch date & progress |
| `CONTENT_GENRE` | Links CONTENT ↔ GENRE |
| `CONTENT_LANGUAGE` | Links CONTENT ↔ LANGUAGE |

 Technologies Used
- MySQL / SQL
- Relational Model Design
- ER Diagram & Normalization
