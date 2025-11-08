# Tech Stack
| Layer              | Technology                      | Purpose                                                 |
| ------------------ | ------------------------------- | ------------------------------------------------------- |
| **Frontend**       | React Native                    | Cross-platform app for iOS & Android                    |
| **Backend**        | Node.js + Express (or NestJS)   | REST API for workouts, health data, and user management |
| **Database**       | PostgreSQL                      | Store user data, workout logs, and nutrition entries    |
| **Storage**        | AWS S3 / Firebase Storage       | For user images, meal photos, etc.                      |
| **Notifications**  | Firebase Cloud Messaging / APNs | Send reminders, challenges, and alerts                  |
| **Authentication** | Firebase Auth or Auth0          | Manage secure user sessions                             |
| **Analytics**      | Firebase / Google Analytics     | Track engagement and progress trends 

# System Components

### 1. Mobile App (React Native)
- Displays workout plans, health dashboards, and meal tracking.  
- Caches user data locally for offline access.  
- Syncs progress and new entries automatically when online.  
- Manages reminders and push notifications.
- Fetches data from the backend API

### 2. Backend API
Handles all business logic:
- Connects to the database
- Workout & challenge management  
- Nutrition recommendations  
- Health data (blood pressure, sugar, cycle) tracking  
- Goal progress calculations  

Additional features:
- Exposes **REST endpoints** for CRUD operations.  
- Integrates with external APIs (e.g., fitness or nutrition databases).

### 3. Database (PostgreSQL)
**Key tables:**
- `users` (profile info, goals)  
- `workouts` (title, duration, category, intensity)  
- `challenges` (progress tracking)  
- `health_metrics` (metric_type, value, timestamp)  
- `meals` (calorie, macro data)  
- `reminders` (user_id, message, trigger_time)

### 4. Notification Service
Sends push notifications for:
- Daily workout reminders  
- Hydration alerts  
- Period or health check reminders  
- Challenge progress updates

### 5. Analytics Layer
- Collects anonymized usage data.  
- Tracks active users, goal completions, and retention.  
- Used for improving personalization algorithms.