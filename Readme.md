## **DESIGN DB MODEL FOR GUVI ZEN CLASS**

The Guvi Zen Class Database Model is designed to manage and streamline the operations of an educational platform. The model encompasses various entities, including users, students, mentors, courses, topics, tasks, attendance, and feedback, each represented by a dedicated table in the database. The model aims to achieve a high level of normalization, ensuring data integrity and minimizing redundancy.

### Key Components:

1. **Users**:The `Users` table serves as the central repository for basic user information, including the user's ID, name, email, and user type (either 'student' or 'mentor'). This table acts as the parent table, linking to specific student and mentor details, thereby reducing data redundancy and ensuring that common attributes are stored centrally.
2. **Students and Mentors**:Separate tables, `Students` and `Mentors`, store additional, role-specific details. The `Students` table includes student-specific data like phone numbers, linked to the `Users` table via `user_id`. Similarly, the `Mentors` table captures mentor-specific details such as qualifications and years of experience. By separating this data, the model adheres to the principles of normalization, avoiding the duplication of common user data.
3. **Courses and Topics**:The `Courses` table stores course-related information, including the course name, duration, and the mentor responsible for the course. Each course consists of multiple topics, which are managed in the `Topics` table. This table tracks individual topics under each course, specifying the number of sessions required. This hierarchical structure allows for a clear and organized representation of the curriculum.
4. **Tasks**:The `Tasks` table is designed to handle assignments given to students. Each task is linked to a specific topic and student, recording details such as task creation date, description, total marks, and the student's performance. This structure supports detailed tracking of student progress and performance across different subjects.
5. **Attendance and Feedback**:
   The `Attendance` table monitors student attendance for each topic, capturing the attendance status for specific dates. The `Feedback` table, on the other hand, collects student feedback on topics, allowing for quality assessment and continuous improvement of the educational content.
