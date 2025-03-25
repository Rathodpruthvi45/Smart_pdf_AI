# Smart PDF Question Maker

An AI-powered application that generates questions from PDF documents for studying, exam preparation, and knowledge assessment.

## Features

- **PDF Upload & Processing**: Upload PDFs and extract content for question generation
- **AI Question Generation**: Generate multiple-choice and descriptive questions from PDF content
- **Question Management**: View, save, and export generated questions
- **User Authentication**: Secure login and registration system
- **Subscription Tiers**: Free, Pro, and Enterprise plans with different usage limits
- **Admin Dashboard**: Monitor users, PDFs, and platform usage statistics

## Technology Stack

### Backend

- FastAPI (Python web framework)
- PostgreSQL (Database)
- LangChain (AI framework)
- Hugging Face Models (AI text generation)
- JWT Authentication

### Frontend

- React.js
- React Router
- Context API for state management
- Modern CSS with responsive design

## Installation

### Prerequisites

- Node.js (v14+)
- Python (v3.8+)
- PostgreSQL

### Backend Setup

1. Clone the repository

   ```
   git clone https://github.com/Rathodpruthvi45/Smart_pdf_AI.git
   cd smart-pdf-question-maker
   ```

2. Create and activate virtual environment

   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies

   ```
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the backend directory with:

   ```
   DATABASE_URL=postgresql://username:password@localhost:5432/dbname
   SECRET_KEY=your_secret_key
   HUGGINGFACE_API_TOKEN=your_huggingface_token
   ```

5. Start the backend server
   ```
   cd backend
   uvicorn app.main:app --reload
   ```

### Frontend Setup

1. Navigate to the frontend directory

   ```
   cd frontend
   ```

2. Install dependencies

   ```
   npm install
   ```

3. Start the development server

   ```
   npm start
   ```

4. Open your browser and navigate to http://localhost:3000

## Usage

1. **Account Creation**: Register for a new account or log in with existing credentials
2. **Upload PDF**: Navigate to the upload page and select a PDF file
3. **Select Question Types**: Choose between multiple-choice, descriptive, or both
4. **Generate Questions**: Specify the number of questions to generate
5. **View & Export**: Review generated questions, customize them if needed, and export

## API Endpoints

- `POST /api/v1/upload-pdf` - Upload a PDF document
- `POST /api/v1/generate-questions` - Generate questions from a PDF
- `POST /api/v1/auth/register` - Register a new user
- `POST /api/v1/auth/login` - Authenticate a user
- `GET /api/v1/admin/dashboard` - Get admin dashboard statistics

## Subscription Tiers

- **Free**: Up to 3 PDFs, limited questions per month
- **Pro**: Up to 10 PDFs, more questions per month
- **Enterprise**: Unlimited PDFs and questions

## Screenshots

(Include screenshots of the application here)

## Project Structure

```
smart-pdf-question-maker/
├── backend/                 # FastAPI backend
│   ├── app/
│   │   ├── api/             # API endpoints
│   │   ├── core/            # Core functionality
│   │   ├── models/          # Data models
│   │   └── main.py          # Entry point
│   └── requirements.txt     # Python dependencies
│
├── frontend/                # React frontend
│   ├── public/              # Static files
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── context/         # Context providers
│   │   ├── pages/           # Page components
│   │   ├── styles/          # CSS files
│   │   └── App.js           # Main component
│   └── package.json         # Node dependencies
│
├── vectorstores/           # Stores processed PDF data
└── README.md               # Project documentation
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Your Name - pruthvirathod4545@gmail.com
web site -https://my-portfolio-q28z.onrender.com/
