# Cloud-Computing
Capstone Project - Cloud Computing Learning Path

## Database Schema GymToolKit
### Table: Users
This table stores information about the users of the application.
| Column   | Type | Constraint     |
|--------|------|----------|
| user_id   | VARCHAR(50)   | PRIMARY KEY, AUTO INCREMENT  |
| username   | VARCHAR(50)   | NOT NULL  |
| email    | VARCHAR(100)   | NOT NULL |
| password   | VARCHAR(50)   | NOT NULL  |
| avatar_url    | VARCHAR(255)   | NOT NULL |

### Table: Tools
This table stores information about the tools available in the application.
| Column   | Type | Constraint     |
|--------|------|----------|
| tools_id   | VARCHAR(255)   | PRIMARY KEY, AUTO INCREMENT  |
| tools_name   | VARCHAR(50)   | NOT NULL  |
| video_url    | VARCHAR(255)   | NOT NULL |
| photo_url   | BYTEA   | NOT NULL  |
| tools_step    | TEXT[ARRAY]   | NOT NULL |
| tools_description    | TEXT   | NOT NULL |
| tags    | TEXT[ARRAY]   | NOT NULL |

### Table: Feedback
This table stores information about the feedback from users of the application.
| Column   | Type | Constraint     |
|--------|------|----------|
| feedback_id   | VARCHAR(50)   | PRIMARY KEY, AUTO INCREMENT  |
| user_rating    | INT   | NOT NULL |
| user_feedback   | TEXT   |   |
| FOREIGN KEY   | (user_id)   | REFERENCES users(user_id)  |
