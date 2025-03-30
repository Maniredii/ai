# **AI Career Mentor**

An intelligent career development platform that provides personalized guidance, resume analysis, and interview preparation using advanced AI technology.

## Features

### 1. AI-Powered Resume Analysis
- Upload and analyze resumes in PDF, DOC, and DOCX formats
- Deep learning-based analysis using DeepSeek-V3 model
- Detailed insights including:
  - Technical and soft skills identification
  - Years of experience calculation
  - Education details extraction
  - Project highlights
  - Formatting suggestions
  - Recommended job roles

### 2. Mock Interview System
- AI-generated interview questions based on your profile
- Real-time feedback on responses
- Performance analysis including:
  - Confidence level
  - Communication skills
  - Technical accuracy
  - Areas for improvement

### 3. Job Recommendations
- Personalized job suggestions based on resume analysis
- Match score calculation
- Required skills identification
- Salary range information
- Location-based recommendations

### 4. User Authentication
- Secure login and registration
- JWT-based authentication
- Protected routes and API endpoints

## Tech Stack

### Frontend
- React.js
- Material-UI for components
- Axios for API calls
- Context API for state management

### Backend
- Node.js with Express
- MongoDB for database
- JWT for authentication
- Multer for file uploads

### AI/ML
- DeepSeek-V3-0324 model for resume analysis
- Transformers library for NLP
- PyPDF2 and python-docx for document processing

## Prerequisites

- Node.js (v14 or higher)
- Python 3.8 or higher
- MongoDB
- Git

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ai-career-mentor.git
cd ai-career-mentor
```

2. Install backend dependencies:
```bash
npm install
```

3. Install frontend dependencies:
```bash
cd client
npm install
cd ..
```

4. Install Python dependencies:
```bash
pip install transformers torch PyPDF2 python-docx
```

5. Create a `.env` file in the root directory:
```env
MONGODB_URI=mongodb://127.0.0.1:27017/career-mentor
JWT_SECRET=your_jwt_secret_here
PORT=5000
NODE_ENV=development
```

## Running the Application

1. Start MongoDB:
```bash
mongod
```

2. Start the development servers:
```bash
npm run dev
```

This will start:
- Backend server on http://localhost:5000
- Frontend development server on http://localhost:3000

## Project Structure

```
ai-career-mentor/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── context/       # Context providers
│   │   └── App.js         # Main application component
│   └── package.json
├── server/                 # Backend Node.js application
│   ├── routes/            # API routes
│   ├── models/            # MongoDB models
│   ├── middleware/        # Custom middleware
│   └── server.js          # Main server file
├── uploads/               # File upload directory
├── ai_analyzer.py         # AI analysis script
├── extract_text.py        # Text extraction script
├── package.json
└── README.md
```

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user
- GET `/api/auth/verify` - Verify JWT token

### Resume Analysis
- POST `/api/resume/upload` - Upload and analyze resume
- GET `/api/resume/analysis` - Get resume analysis results

### Mock Interviews
- POST `/api/interview/start` - Start a new mock interview
- POST `/api/interview/submit/:userId` - Submit interview recording
- GET `/api/interview/feedback/:userId` - Get interview feedback

### Job Recommendations
- GET `/api/jobs/recommendations` - Get personalized job recommendations

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- DeepSeek AI for providing the language model
- Material-UI for the component library
- MongoDB for the database solution
- All contributors and maintainers

## Support

For support, email support@aicareermentor.com or create an issue in the repository. 
