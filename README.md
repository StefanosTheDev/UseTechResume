# UseTechResume



### API Endpoints
- **User Authentication**
  - `POST /api/v1/auth/register` - Register a new user
  - `POST /api/v1/auth/login` - Login an existing user
  - `POST /api/v1/auth/logout` - Logout the current user


- **Resume Management**
  - `GET /api/v1/resumes` - Retrieve all resumes for a user
  - `POST /api/v1/resumes` - Create a new resume
  - `GET /api/v1/resumes/{id}` - Retrieve a specific resume by ID
  - `PUT /api/v1/resumes/{id}` - Update a specific resume
  - `DELETE /api/v1/resumes/{id}` - Delete a specific resume

- **AI Text Suggestions**
  - `POST /api/v1/suggestions` - Get AI-powered text suggestions for improving resume content
 
