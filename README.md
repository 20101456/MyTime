# MyTime
Software Engineering Practice

Product Vision
Our product is aimed for college students and lecturers who are looking for a solution to manage their class schedules.
MyTime is a timetabling and scheduling application that helps students and lecturers in SETU to plan their academic and personal lives. It shows them their class time, subject, and room number for each course, as well as the availability of other facilities such as computer labs, libraries, and study rooms.

Different from The SETU Website and Moodle, our product makes scheduling more accessible and personalised to everyone’s needs.

Revised Feature List (Unchanged)

1.	Class Schedule Management: Allows students and lecturers to input and view their class schedules in a user-friendly format.

2.	Assignment Tracker: Helps users keep track of assignment due dates and progress.

3.	Study Session Planner: Enables users to plan and manage their study sessions effectively.

4.	Notifications and Reminders: Sends timely reminders for upcoming classes, assignments, and study sessions.

5.	Integration with Academic Calendar: Syncs with the academic calendar to automatically update for holidays, exam periods, etc.

6.	Personalized User Profiles: Allows for customization based on the user’s role (student or lecturer), courses, and preferences.

7.	Cross-Platform Accessibility: Ensures the app is accessible on various devices and platforms for convenience.

8.	Lecturer Office Hours: Allows lecturers to set and students to view office hours.

9.	College Resources: Provides a space for sharing course-related resources and materials.
We looked at resources already available at the college such as Moodle and the SETU website and found them unintuitive and not very accessible. We want to make it is easier to access these features for general use by the students. Our hope is that if students can easily access resources like the Maths Help Centre for example, they will get the help needed to excel in their studies.

Personas
What is a Persona?

A persona is a fictional character created to represent a user type that might use a site, brand, or product in a similar way. Personas are used to help guide decisions about a product, such as features, interactions, and visual design.
Personas are extremely useful in giving a human face to an otherwise abstract user base. They typically include demographic information, behaviours, needs, and pain points.

Persona 1
Bella
Role: Undergraduate Student
Age: 20
Course: Computer Science
Needs: Wants to manage her time effectively between classes, assignments, part-time job, and social life.
Pain Points: Often forgets assignment due dates and struggles to balance academic and personal life.
How MyTime Helps: MyTime helps Bella stay on top of her academic responsibilities. The class schedule management feature allows her to plan her part-time job and social activities around her classes.

Persona 2

Oliver
Role: Lecturer
Age: 35
Course: Biomolecular with Pharmaceutical Science
Needs: Wants to keep track of his teaching schedule and office hours.
Pain Points: Has difficulty managing office hours and ensuring students are aware of them.
How MyTime Helps: MyTime allows Oliver to efficiently manage his teaching responsibilities and communicate his availability to students.

Persona 3
Gina
Role: Postgraduate Student
Age: 24
Course: Business
Needs: Would like to coordinate study sessions with her project group members.
Pain Points: Struggles to find free classrooms for her and her project group to work in.
How MyTime Helps: MyTime will enable Gina to plan and coordinate study sessions effectively with her group.

Scenarios
What is a Scenario?
A user scenario describes the processes a user goes through to complete a task using a product, system, or service.
User scenarios are typically used in product development and user-centred design to help understand and cater to the user’s needs. They provide insights into the user’s motivations, expectations, and goals, and can help guide the design and development process.

Scenario 1
Class Schedule Setup
User Persona: Bella
Goal: Bella wants to input her class schedule into the app at the start of the semester.
Steps to Achieve the Goal:
	Bella opens the MyTime app.
	She navigates to the Class Schedule Management feature.
	Bella inputs the details of her classes, including the course name, time, and location.
	The MyTime app saves Bella’s class schedule and displays it in a user-friendly format.

Scenario 2
Assignment Tracking
User Persona: Oliver
Goal: Oliver wants to set a reminder for grading assignments.
Steps to Achieve the Goal:
	Oliver opens the MyTime app.
	He navigates to the Assignment Tracker feature.
	Oliver inputs the details of the assignment grading deadline.
	He sets a reminder for the grading deadline.
	The MyTime app will send Oliver a notification about the upcoming grading deadline.

Scenario 3
Study Session Planning
User Persona: Gina
Goal: Gina wants to schedule a group study session for her project group.
Steps to Achieve the Goal:
	Gina opens the MyTime app.
	She navigates to the Study Session Planner feature.
	Gina inputs the details of the study session, including the date, time, participants and the location/room.
	She shares the study session details with her project group.
	The MyTime app sends Gina and her project group notifications about the upcoming study session.

User Stories
What is a User Story?
User Story 1
As a student, I want to input my class schedule into MyTime so that I can easily access my timetable and room locations.
User Story 2
As a lecturer, I want to be able to view and manage my teaching schedule on MyTime to organize my academic responsibilities efficiently.
User Story 3
As a student, I want MyTime to track my assignments and remind me of due dates so that I never miss a deadline.
User Story 4
As a student, I want to plan my study sessions using MyTime to ensure I allocate enough time for each subject.
User Story 5
As a user, I want MyTime to sync with the academic calendar so that my schedule automatically adjusts for holidays and exam periods.
User Story 6
As a new user, I want to create a personalized profile on MyTime that reflects my role, courses, and preferences to have a tailored experience.


Junit Testing:

Calendar Class:
package mo.chuid.ama.mytime;

public class Calendar {
    private int day;
    private int month;
    private int year;

    public Calendar(int day, int month, int year) {
        this.day = day;
        this.month = month;
        this.year = year;
    }

    public int getDay() {
        return day;
    }

    public int getMonth() {
        return month;
    }

    public int getYear() {
        return year;
    }
}

package mo.chuid.ama.mytime;

import org.junit.Before;
import org.junit.Test;
import static org.junit.Assert.assertEquals;

public class CalendarTest {
    private Calendar calendar;

    @Before
    public void setUp() {
        calendar = new Calendar(1, 1, 2000);
    }

    @Test
    public void testConstructor() {
        assertEquals(1, calendar.getDay());
        assertEquals(1, calendar.getMonth());
        assertEquals(2000, calendar.getYear());
    }
}



Module Class:
package com.example.softenginpra;

public class Module {
    private String code;
    private String name;

    public Module(String code, String name) {
        this.code = code;
        this.name = name;
    }

    public String getCode() {
        return code;
    }

    public String getName() {
        return name;
    }

    public void setCode(String code) {
        this.code = code;
    }

    public void setName(String name) {
        this.name = name;
    }
}

package com.example.softenginpra;

import org.junit.Before;
import org.junit.Test;
import static org.junit.Assert.*;

public class ModuleTest {
    private Module module;
    
    @Before
    public void setUp() {
        module = new Module("CS101", "Introduction to Computer Science");
    }
    
    @Test
    public void testGetCode() {
        assertEquals("CS101", module.getCode());
    }
    
    @Test
    public void testGetName() {
        assertEquals("Introduction to Computer Science", module.getName());
    }
    
    @Test
    public void testSetCode() {
        module.setCode("CS102");
        assertEquals("CS102", module.getCode());
    }
    
    @Test
    public void testSetName() {
        module.setName("Data Structures");
        assertEquals("Data Structures", module.getName());
    }
}


Use Case
Use Case Diagram
 
UC1: View Schedule
Primary Actor: Student/Lecturer
Preconditions:
•	The user is logged into the MyTime app.
•	The user has a schedule set up in the app.
Main Success Scenario:
10.	User selects the “View Schedule” option.
11.	System retrieves the user’s schedule from the database.
12.	System displays the user’s schedule in a user-friendly format.
Failure Scenarios:
No schedule set up:
•	As above but with the following modifications:
•	At step 2, system finds no schedule for the user.
•	At step 3, system informs the user that no schedule is set up.

UC2: Edit Schedule
Primary Actor: Student/Lecturer
Preconditions:
•	The user is logged into the MyTime app.
•	The user has already set up their schedule and is returning to edit it.
Main Success Scenario:
1.	User selects the “Edit Schedule” option.
2.	System displays the current schedule with options to add or remove classes.
3.	User selects to add a new class and fills out the details (course name, time, location).
4.	User presses submit.
5.	System updates the schedule with the new class.
6.	System redirects user to a page confirming successful schedule update.
Alternative Success Scenarios:
User removes a class:
•	At step 3, user selects to remove a class and chooses the class to be removed.
•	System removes the selected class from the schedule.
Failure Scenarios:
Class time is not valid:
•	As above but with the following modifications:
•	At step 3, user enters a class time that conflicts with an existing class.
•	At step 4, system alerts the user that the class time is invalid and takes the user back to step 3 to re-enter class details.
Failure to update schedule:
•	As above but with the following modifications:
•	At step 5, system fails to update the schedule.
•	Add step 5a: System displays reason for failed update, user is then taken back to step 3 to re-enter class details or try again.

UC3: Set Reminder
Primary Actor: Student/Lecturer
Preconditions:
•	The user is logged into the MyTime app.
•	The user has a schedule set up in the app.
Main Success Scenario:
1.	User selects the “Set Reminder” option.
2.	System displays the current schedule with options to set reminders for each class or task.
3.	User selects a class or task and sets a reminder.
4.	User presses submit.
5.	System updates the schedule with the new reminder.
6.	System confirms successful reminder setup to the user.
Failure Scenarios:
Invalid reminder time:
•	As above but with the following modifications:
•	At step 3, user sets a reminder time that has already passed.
•	At step 4, system alerts the user that the reminder time is invalid and takes the user back to step 3 to re-enter reminder details.
Failure to set reminder:
•	As above but with the following modifications:
•	At step 5, system fails to set the reminder.
•	Add step 5a: System displays reason for failed reminder setup, user is then taken back to step 3 to re-enter reminder details or try again.

UC4: View Assignment Deadlines
Primary Actor: Student
Preconditions:
•	The user is logged into the MyTime app.
•	The user has assignments set up in the app.
Main Success Scenario:
1.	Student selects the “View Assignment Deadlines” option.
2.	System retrieves the student’s assignments from the database.
3.	System displays the assignments with their deadlines.
Failure Scenarios:
No assignments set up:
•	As above but with the following modifications:
•	At step 2, system finds no assignments for the student.
•	At step 3, system informs the student that no assignments are set up.

UC5: Set Office Hours
Primary Actor: Lecturer
Preconditions:
•	The user is logged into the MyTime app.
Main Success Scenario:
1.	Lecturer selects the “Set Office Hours” option.
2.	System displays a form to set office hours.
3.	Lecturer fills out the form with the office hours details.
4.	Lecturer presses submit.
5.	System updates the lecturer’s profile with the new office hours.
6.	System confirms successful office hours setup to the lecturer.
Failure Scenarios:
Invalid office hours:
•	As above but with the following modifications:
•	At step 3, lecturer sets office hours that conflict with their class schedule.
•	At step 4, system alerts the lecturer that the office hours are invalid and takes the lecturer back to step 3 to re-enter office hours details.
Failure to set office hours:
•	As above but with the following modifications:
•	At step 5, system fails to set the office hours.
•	Add step 5a: System displays reason for failed office hours setup, lecturer is then taken back to step 3 to re-enter office hours details or try again.

Activity
Activity Diagram
 
Class
Class Diagram
 
Prototype
What is a Prototype?
A prototype is an early model or release of a product built to test a concept or process. It serves as a tangible representation of a design concept, enabling designers to bring their ideas to life and test them in a practical manner during the research and design phase. 
By creating a prototype, designers can explore the functionality, usability, and overall user experience of their design before investing significant resources into full-scale development. 
This iterative process of testing and refining the prototype allows designers to identify and address any flaws or areas of improvement, leading to a more refined and successful final design

Tool used to create Prototype (say if you found it easy to use or not briefly!!!)
I used a prototyping tool called JustinMind. It is a free desktop app used for high-fidelity prototyping.
My experience with JustinMind was nice, it has a nice UI and was easy to use. It offers an extensive selection of icons and libraries, which significantly simplified the design process. 
Additionally, it provides the flexibility to import external libraries for an even broader range of icons, enhancing the customization possibilities. Overall, JustinMind proved to be an effective tool for my prototyping needs.
URL or Screen Shots (not all some)
 
 
 
