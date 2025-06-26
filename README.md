# PennyWise
A simple Android application that helps users track daily expenses, set budget goals, visualize spending through graphs, and stay motivated using gamification techniques.

## Purpose of the App
PennyWise is designed to simplify personal finance management by allowing users to:

- Record and manage expenses.
- Set budget goals (minimum and maximum limits).
- Visualize spending patterns through interactive graphs.
- Stay motivated with gamification elements.
- Monitor expenses over specific periods.
- Access the app directly from an Android mobile device.

This app was developed as part of a software development project to practice mobile app development, UI/UX design, data visualization, and basic financial tracking functionality.

## Features

### Authentication
- Login and Signup screens.
- Secure user authentication with username and password.

### Expense Management
- Add new expenses with:
  - Date
  - Category
  - Start time
  - End time
  - Description.
- View expenses in a scrollable list (RecyclerView).
- Data Persistence: Data that users input is now captured and stored locally, meaning it remains available even after closing and reopening the app.

### Budget Goals
- Set minimum and maximum budget limits.
- Track if total expenses are within budget.

### Expense Filtering
- Filter expenses by date range.
- Focus on specific periods for analysis.

### Graph Visualization
- Interactive Graphs: Users can now visualize their expenses through bar charts or pie charts.
- This feature helps users easily understand how they spend money across different categories or time periods.

### Gamification (New Feature)
- A Gamification system has been added to keep users motivated:
- Earn badges or points for logging expenses regularly.
- Receive rewards for staying under budget.
- Progress indicators encourage consistent financial tracking.

### Clean and Intuitive UI
- Styled buttons, text fields, and views for seamless navigation.
- View the app on both emulators and real physical mobile devices — fully functional on Android phones.

### Personal Features Implemented from Design Document
- Expense filtering functionality.
- Budget goal tracking with total expense calculation.
- RecyclerView-based expense list for usability.
- Graph visualization for better financial insights.
- Gamification to improve user engagement and retention.

### Functional Views in the App
The following views are fully functional and tested:
- Login Screen – For user authentication.
- Signup Screen – For new user registration.
- Main Dashboard – Displays total expenses, budget status, and navigation options.
- Add Expense Screen – Form to capture expense details.
- Expense List Screen – Displays all recorded expenses.
- Filter Expenses Screen – Allows users to filter expenses by date.
- Graph Screen – Shows bar or pie charts based on expenses (New).
- Gamification Screen / Section – Displays points, badges, and achievements (New).

### Additional Functionalities
#### UserProfileManager
Handles saving and retrieving the user's profile information such as name and bio.

- What It Does:
   - saveProfile(name, bio) – Saves the user's name and bio to local storage using  SharedPreferences.
   - getName() / getBio() – Retrieves the saved name and bio to be displayed or reused.

- Use Case:
   - When a user logs in or updates their profile, this function stores their information. It can be accessed from any part of the app whenever needed.

#### ActivityLogger
Keeps track of user actions within the app, like visiting screens or performing tasks.

- What It Does:
   -logActivity(message) – Saves a timestamped message, such as "Visited MainActivity", to a local activity log.
   - getLog() – Retrieves the entire log of activities for review or display.

- Use Case:
   -Useful for showing the user a history of their actions, helpful for engagement tracking, debugging, or providing activity feedback.

#### Example in App Usage:
- When the user opens MainActivity:
    - "Liam" and "App Developer" are saved as the user's name and bio using UserProfileManager.
    - "Visited MainActivity" is logged as an activity using ActivityLogger.
- Both the profile information and the activity log are displayed on the screen, giving the user clear feedback on their profile and recent activities.

## How to Use
1. Sign Up: Register by providing name, username, and password.
2. Login: Use your credentials to access the app.
3. Add Expenses: Fill in the details and submit.
4. Set Budget Goals: Input minimum and maximum budgets to monitor spending.
5. Filter Expenses: Select start and end dates to view relevant expenses.
6. View Graphs: Navigate to the graph section to visualize your expenses by category or date.
7. Earn Rewards: Log expenses consistently and stay under budget to unlock achievements.
8. View on Mobile: The app is now installable and fully functional on real Android smartphones.

## Installation Instructions
### Prerequisites
- Android Studio (Electric Eel or newer recommended).
- Android SDK 33 or higher.
- Android device or emulator running Android 8.0 (API level 26) or higher.

### Steps
1. Clone the repository:
- git clone https://github.com/MrPREDDY18/PennyWise.git
2. Open the project in Android Studio.
3. Sync Gradle and install any missing dependencies.
4. Connect a physical Android phone via USB with developer mode enabled or use an emulator.
5. Click Run to install and launch the app on your device.

## Demo Video
- Professional Demo Video with Voice-over:
https://youtube.com/shorts/Clux5bNJmgs
- A compressed version of the video is included in the ZIP submission.

## Research and Design Documents
- Included in the /docs folder:
  - Design Document (UI Wireframes, App Flow, Database Design)
  - Research Document (Technology Choices, Tools, Market Research)
  - Design Justifications (Why certain features and UI decisions were made)

## Project Structure

---

## Project Structure

/app  
 ├── java/com/yourpackage  
 │    ├── LoginActivity.java  
 │    ├── SignupActivity.java  
 │    ├── MainActivity.java  
 │    ├── ExpenseEntryActivity.java  
 │    ├── ExpenseFilterActivity.java  
 │    ├── GraphActivity.java  
 │    ├── GamificationActivity.java  
 │    ├── UserProfileManager.java  
 │    ├── ActivityLogger.java  
 │    └── ... (other activities)  
 ├── res/  
 │    ├── layout/  
 │    ├── drawable/  
 │    └── values/  
 └── AndroidManifest.xml  

/docs  
 ├── design_document.pdf  
 ├── research_document.pdf  
 └── other_files.pdf  

---


## Code Quality
- Inline Comments: Meaningful comments added to explain the logic and structure.
- Logging: Implemented Log.d() throughout for debugging and clarity.
- Tested on Physical Devices: The app now runs successfully on real Android devices, not just emulators.

## GitHub Repository
Public GitHub Repo: https://github.com/MrPREDDY18/PennyWise.git 

## Continuous Integration 
- GitHub Actions can be added using .github/workflows/android.yml to automate:
  - Build checks
  - Unit tests (if implemented)
  - Lint checks

## Future Enhancements
- Add cloud storage using Firebase for data synchronization.
- Implement user profiles and multi-user support.
- Notifications and reminders for budget limits.
- Dark mode theme.
- More gamification features like leaderboards or streak tracking.
