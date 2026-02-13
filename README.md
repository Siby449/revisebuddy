# ReviseBuddy
StudyBuddy – Revision Tracker Web Application
T Level Year 2 – Digital Production, Design and Development

Project Title: StudyBuddy
Developer: Sibtain Rafi
Time Allocation: Up to 8 hours
Qualification: T Level – Occupational Specialism Preparation

 Project Overview

StudyBuddy is a Django-based web application designed to help students organise and track their revision topics.

Users can securely register, log in, and manage their own revision topics. The system ensures that each user can only access and modify their own data.

This project demonstrates core web development skills including authentication, database design, CRUD operations, validation, and testing.

 Features
Core Features (Implemented)

User registration

User login and logout

Secure authentication and authorisation

Create, view, update and delete revision topics (CRUD)

User-specific data protection

Search topics by keyword

Filter topics by status and priority

Dashboard displaying:

Total number of topics

Breakdown by status

Progress overview

Topic Fields

Each revision topic includes:

Title (Required)

Description (Optional)

Status

Not Started

In Progress

Confident

Priority

Low

Medium

High

Validation

Title cannot be blank

Form validation prevents invalid submissions

Users cannot access other users’ data

 Stretch Module Implemented
Module A – Due Dates

Added a due date field to each topic

Overdue topics are automatically highlighted

Dashboard displays overdue topic count

This demonstrates additional model fields, logic handling, and conditional template rendering.

 Technologies Used

Python 3

Django 4+

SQLite (default Django database)

HTML

CSS

Git (version control)

 Database Design

Main model:

Topic Model

id (Primary Key)

user (ForeignKey to User)

title (CharField)

description (TextField)

status (CharField with choices)

priority (CharField with choices)

due_date (DateField – Stretch Module)

created_at (DateTimeField)

Relationships:

One User → Many Topics

Topics linked securely using ForeignKey

 Security & Authorisation

Django’s built-in authentication system used

Login required for all topic views

Querysets filtered by logged-in user

CSRF protection enabled

LoginRequiredMixin used for class-based views

 Search & Filtering

Users can:

Search topics by title keyword

Filter by status

Filter by priority

Combine filters for refined results

 Dashboard

The dashboard provides:

Total number of topics

Number of:

Not Started

In Progress

Confident

Overdue topics (Stretch Module)

Visual progress summary

 Testing
Manual Testing

A manual test plan with at least 8 test cases is included separately.

Example test cases include:

Register new user

Login with valid credentials

Login with invalid credentials

Create topic with valid data

Attempt to create topic with blank title

Edit topic successfully

Delete topic

Attempt to access another user’s topic

Search functionality

Filter functionality
