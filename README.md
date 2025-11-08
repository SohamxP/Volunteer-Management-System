# Volunteer Management System (Console, Java)

A terminal-based Volunteer Management System (VMS) with:
- Admin and Volunteer roles (login/registration)
- Event creation/scheduling
- Volunteer sign-ups
- Attendance tracking
- Reporting (event summary, volunteer hours)
- File-based persistence (CSV in `data/`)

## Project Layout
```
VMS_Console_Java/
  ├─ src/
  │  └─ vms/
  │     ├─ Main.java
  │     ├─ model/
  │     │  ├─ User.java
  │     │  ├─ Admin.java
  │     │  ├─ Volunteer.java
  │     │  ├─ Event.java
  │     │  ├─ Signup.java
  │     │  └─ Attendance.java
  │     ├─ service/
  │     │  ├─ DataStore.java
  │     │  ├─ AuthService.java
  │     │  ├─ EventService.java
  │     │  ├─ VolunteerService.java
  │     │  └─ AttendanceService.java
  │     └─ util/
  │        └─ CSV.java
  └─ data/
     ├─ users.csv
     ├─ events.csv
     ├─ signups.csv
     └─ attendance.csv
```

## Requirements
- Java 17+ (works with Java 11+ too)

## Compile
From the project root:
```bash
javac -d out $(find src -name "*.java")
```

## Run
```bash
java -cp out vms.Main
```

## Default Admin
- Email: admin@vms.local
- Password: admin123

You can change or add admins directly in `data/users.csv` (role = ADMIN).
