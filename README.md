# Lab Management System

Desktop application for managing lab evaluations in an Outcome Based Education setup. The project is built with Windows Forms in C# on the frontend and SQL Server on the backend.

## Project Overview

Department of Computer Science UET Lahore follows Outcome Based Education, where each subject is mapped to multiple CLOs. For lab work, those CLOs are further mapped to rubrics. This application streamlines the manual evaluation process by letting the teacher manage students, CLOs, rubrics, assessment components, rubric levels, attendance, and student results from one place.

The system also calculates obtained marks automatically from the assigned rubric level using the component marks and the maximum rubric level.

## Features

- Manage students
- Manage CLOs
- Manage rubrics
- Manage rubric levels
- Manage assessments
- Manage assessment components
- Mark student evaluations
- Manage student attendance
- View and store student results
- Automatic mark calculation from rubric level

## Tech Stack

- Frontend: C# Windows Forms
- Backend: Microsoft SQL Server
- Framework: .NET Framework 4.7.2

## Database Structure

The SQL script creates the following tables:

- Lookup
- Clo
- ClassAttendance
- Assessment
- Rubric
- Student
- RubricLevel
- AssessmentComponent
- StudentAttendance
- StudentResult

## How It Works

1. A teacher creates CLOs, rubrics, rubric levels, and assessments.
2. Each assessment is divided into assessment components with assigned marks.
3. A student is evaluated against a rubric level for each component.
4. The application calculates the obtained marks automatically using:

   Obtained Marks = (Obtained Rubric Level / Max Rubric Level) x Component Marks

5. The calculated results are stored for later review and reporting.

## Prerequisites

- Visual Studio with Windows Forms support
- .NET Framework 4.7.2
- SQL Server
- SQL Server Management Studio, or another tool to run the database script

## Setup Instructions

1. Open and run `Database-Script.sql` in SQL Server.
2. Create or confirm the database named `ProjectB`.
3. Update the connection string in the project code if your SQL Server instance name differs from `AHMAD-HP`.
4. Open `Lab-Management-System.sln` in Visual Studio.
5. Build and run the project.

## Configuration Notes

The application currently connects to SQL Server with the following pattern:

Data Source = AHMAD-HP; Initial Catalog = ProjectB; Integrated Security = True;

If you are running the project on another machine, change the server name and database name to match your local SQL Server setup.

## Application Start

The program starts from the `HomePage` form and provides navigation to the main modules from there.

## Project Files

- `Lab-Management-System.sln` - Visual Studio solution
- `Lab-Management-System.csproj` - Windows Forms project file
- `Database-Script.sql` - SQL Server schema and database script

## Course Details

- Course: Database System Lab
- Semester: 2nd
- Project: Mid Term
