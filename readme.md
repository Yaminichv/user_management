# User Management System 📋🚀

Welcome to the **User Management System** project, an open-source repository that serves as the backbone for managing users efficiently. This project introduces robust functionalities such as user creation, authentication, validation, search, and filtering, alongside resolving critical bugs and enhancing feature performance.

---

## Key Features ✨
 **User Search and Filtering**:  
   - Implements a comprehensive user search feature based on multiple parameters (e.g., name, email).  
   - Adds efficient filtering options for admins to manage user data effortlessly.
## Quality Assurance 

1. **Email Verification**:  
   - Fixes critical email verification errors for users with `None` user-IDs.  
   - Ensures proper token generation and validation during the email verification process.

2. **Duplicate Email/Nickname Validation**:  
   - Prevents the creation or update of users with duplicate emails or nicknames.  
   - Enhances data integrity and avoids user conflicts.

3. **Password Strength Validation**:  
   - Implements password validation checks ensuring strong passwords during user creation.  
   - Criteria include uppercase, lowercase, numbers, and special characters.

4. **Docker Build Optimization**:  
   - Resolves Docker build issues for seamless CI/CD deployment.

5. **Dependency Conflict Resolutions**:  
   - Fixes conflicts arising from incompatible Python dependencies.  
   - Improves pipeline stability for testing and deployment.

---

## Installation ⚙️

Follow these steps to set up the project locally:

### Prerequisites:
- Python 3.10+
- Docker and Docker Compose
- MinIO for object storage (Optional)

### Steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Yaminichv/user_management.git
   cd user_management
   ```

2. **Setup the Environment**:
   Install required Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Docker Services**:
   Ensure Docker is running and execute:
   ```bash
   docker compose up --build -d
   ```

4. **Run Migrations**:
   Apply database migrations:
   ```bash
   alembic upgrade head
   ```

5. **Access the Application**:
   The application will be available at `http://localhost`.

---

## Testing 🧪

Run the test suite to ensure all features work correctly:
```bash
pytest --cov=app tests/
```

---

## Closed Issues ✅

### Bugs:
1. **#12**: Role downgrade during email verification for non-anonymous users.  
2. **#10**: Duplicate email/nickname validation during user update.  
3. **#8**: Email verification fails due to user-id being `None`.  
4. **#6**: Validate password strength while user creation.  
5. **#3**: Dependency conflict in scanning the image.  
6. **#1**: Docker build issue.

### Enhancements:
- **#14**: User Search and Filtering.

---

## Contribution Guidelines 🤝
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes and submit a PR.

---

## Deployment 🌐

The project is Dockerized for deployment. Follow these steps for deployment on DockerHub:
```bash
docker build -t your_dockerhub_username/user_management .
docker push your_dockerhub_username/user_management
```

## DockerHub Repository URL
https://hub.docker.com/r/yaminichowdary996/user_management

---

## License 📄
This project is licensed under the MIT License.

---

