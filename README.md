# ScholarHub - Research Management Platform

A comprehensive platform for managing academic research projects, notes, references, and files.

## Features

- 📊 Research project management
- 📝 Rich text note-taking
- 📚 Reference management
- 📁 File storage (PDF, DOCX, EPUB) with 100MB limit per user
- ⏰ Task and deadline tracking
- 🌓 Dark/Light theme support

## Tech Stack

- React 18 with TypeScript
- Tailwind CSS for styling
- MySQL for database
- Node.js and Express for backend
- JWT for authentication
- Vite for development and building

## Prerequisites

Before installation, ensure you have:

- Node.js >= 18
- npm >= 9
- MySQL >= 8.0
- Git (for cloning the repository)

## Installation Guide

### 1. Clone and Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/scholarhub.git
cd scholarhub

# Install dependencies
npm install
```

### 2. Installation Wizard

ScholarHub comes with an interactive installation wizard that guides you through the setup process:

1. **Database Configuration**
   - Host: Your MySQL server host
   - Port: MySQL port (default: 3306)
   - Username: Database user with create/modify privileges
   - Password: Database user password
   - Database Name: Name for the ScholarHub database

2. **Administrator Account**
   - Full Name: Admin user's full name
   - Email: Admin login email
   - Password: Secure password (minimum 8 characters)

3. **Installation Process**
   The wizard will automatically:
   - Create and configure the database
   - Set up necessary tables
   - Create the admin account
   - Configure system settings

### 3. Development Server

After installation is complete, start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## Project Structure

```
scholarhub/
├── src/
│   ├── components/     # Reusable UI components
│   ├── contexts/       # React contexts
│   ├── lib/           # Core functionality
│   │   ├── api/       # API client functions
│   │   ├── db/        # Database utilities
│   │   └── server/    # Server-side logic
│   ├── pages/         # Page components
│   └── types/         # TypeScript definitions
├── public/            # Static assets
└── .env.example       # Environment variables template
```

## Environment Variables

Copy `.env.example` to `.env` and configure:

```env
# Database Configuration
DB_HOST=localhost
DB_PORT=3306
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=scholarhub

# Authentication
JWT_SECRET=your-secure-jwt-secret
JWT_EXPIRES_IN=24h

# File Storage
MAX_FILE_SIZE=104857600  # 100MB in bytes
UPLOAD_DIR=uploads

# Server Configuration
PORT=3000
NODE_ENV=development
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## File Storage

The application supports:
- File types: PDF, DOCX, EPUB
- Maximum file size: 100MB per user
- Automatic file type validation
- Secure file storage

## Database Schema

The MySQL database includes the following tables:

- `users` - User accounts and profiles
- `projects` - Research projects
- `notes` - Research notes with rich text
- `references` - Bibliography and citations
- `files` - Uploaded document metadata
- `deadlines` - Project deadlines and tasks

## Contributing

1. Fork the repository
2. Create your feature branch:
```bash
git checkout -b feature/amazing-feature
```
3. Commit your changes:
```bash
git commit -m 'Add some amazing feature'
```
4. Push to the branch:
```bash
git push origin feature/amazing-feature
```
5. Open a Pull Request

## Troubleshooting

### Installation Issues

1. **Database Connection Fails**
   - Verify MySQL is running
   - Check credentials in database configuration
   - Ensure database user has sufficient privileges
   - Confirm firewall settings allow connection

2. **Admin Account Creation Fails**
   - Ensure password meets minimum requirements (8+ characters)
   - Verify email format is valid
   - Check database connection is stable

3. **Development Server Issues**
   - Verify all dependencies are installed
   - Check port 5173 is available
   - Ensure environment variables are set correctly

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, please open an issue in the GitHub repository.
