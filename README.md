# AstroBlog
![image](https://github.com/user-attachments/assets/53735e55-cbf2-4722-b1ec-75b7be9afe94)



# Crypto Streets Blog

A modern, full-stack blog platform built with Astro and Go, featuring real-time content management, user authentication, and a responsive design optimized for crypto and blockchain content.

## 🌟 Features

### Frontend (Astro)
- **Modern UI/UX**: Clean, responsive design with CSS Grid and Flexbox
- **Server-Side Rendering (SSR)**: Fast loading and SEO-optimized pages
- **Rich Text Editor**: Quill.js integration for creating formatted blog posts
- **Dynamic Content**: Real-time blog post fetching and display
- **View Counter**: Track and display article views
- **SEO Optimized**: Meta tags, structured data, and clean URLs

### Backend (Go)
- **RESTful API**: Complete CRUD operations for blog posts
- **User Authentication**: JWT-based authentication system
- **Database Integration**: MySQL database with connection pooling
- **CORS Support**: Cross-origin resource sharing for frontend integration
- **View Tracking**: Real-time view count updates

### Key Functionality
- Create, read, update, and delete blog posts
- User authentication and authorization
- Real-time view counting
- Responsive design for all devices
- Docker containerization for easy deployment
- API endpoints for external integrations

## 🛠️ Tech Stack

### Frontend
- **Astro** - Modern static site generator with SSR capabilities
- **TypeScript** - Type-safe JavaScript development
- **CSS3** - Custom styling with modern layout techniques
- **Quill.js** - Rich text editor for content creation

### Backend
- **Go (Golang)** - High-performance server-side language
- **Gin** - Fast HTTP web framework
- **MySQL** - Relational database for data persistence
- **JWT** - JSON Web Tokens for authentication
- **CORS** - Cross-origin resource sharing middleware

### DevOps
- **Docker** - Containerization for consistent deployment
- **Docker Compose** - Multi-container orchestration
- **Node.js** - Runtime environment for Astro

## 📁 Project Structure

```
├── blog/                    # Astro frontend application
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── layouts/         # Page layouts and templates
│   │   ├── lib/            # Utility functions and helpers
│   │   ├── pages/          # Astro pages and routes
│   │   └── style.css       # Global styles
│   ├── public/             # Static assets
│   ├── astro.config.mjs    # Astro configuration
│   ├── package.json        # Frontend dependencies
│   └── Dockerfile          # Frontend containerization
├── server/                 # Go backend application
│   ├── routes/             # API route handlers
│   ├── models/             # Data models and structures
│   ├── db/                 # Database connection and queries
│   ├── main.go             # Server entry point
│   ├── go.mod              # Go module dependencies
│   └── Dockerfile          # Backend containerization
├── docker-compose.yml      # Multi-container orchestration
└── README.md              # Project documentation
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- Go (v1.23 or higher)
- MySQL database
- Docker and Docker Compose (for containerized deployment)

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd blog
   ```

2. **Frontend Setup**
   ```bash
   cd blog
   npm install
   npm run dev
   ```
   The frontend will be available at `http://localhost:4321`

3. **Backend Setup**
   ```bash
   cd server
   go mod download
   go run main.go
   ```
   The backend API will be available at `http://localhost:8181`

### Environment Configuration

Create a `.env` file in the server directory:
```env
DB_HOST=localhost
DB_PORT=3306
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=blog_db
JWT_SECRET=your_jwt_secret_key
```

### Database Setup

1. Create a MySQL database named `blog_db`
2. Import the database schema (if provided)
3. Update the environment variables with your database credentials

## 🐳 Docker Deployment

### Using Docker Compose (Recommended)

1. **Build and run all services**
   ```bash
   docker-compose up --build
   ```

2. **Access the application**
   - Frontend: `http://localhost:4321`
   - Backend API: `http://localhost:8181`

### Individual Container Deployment

**Frontend:**
```bash
cd blog
docker build -t crypto-blog-frontend .
docker run -p 4321:4321 crypto-blog-frontend
```

**Backend:**
```bash
cd server
docker build -t crypto-blog-backend .
docker run -p 8181:8181 crypto-blog-backend
```

## 📚 API Endpoints

### Blog Posts
- `GET /go-api/getposts` - Fetch main blog posts
- `GET /go-api/getbottomposts` - Fetch bottom/featured posts
- `POST /go-api/createpost` - Create new blog post
- `GET /go-api/getviewcount?slug={slug}` - Get post view count
- `POST /go-api/UpdateViewCount` - Update post view count

### Authentication
- `GET /api/auth` - Verify user authentication
- `POST /api/login` - User login
- `POST /api/logout` - User logout

## 🎨 Customization

### Styling
- Modify `blog/src/style.css` for global styles
- Component-specific styles are in their respective `.astro` files
- The design uses CSS Grid and Flexbox for responsive layouts

### Content Management
- Blog posts are created through the `/post` page
- Rich text editing is powered by Quill.js
- Images and media can be embedded in posts

### Configuration
- Update `astro.config.mjs` for Astro-specific settings
- Modify `server/main.go` for server configuration
- Environment variables control database and JWT settings

## 🔧 Development Scripts

### Frontend (blog directory)
```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
```

### Backend (server directory)
```bash
go run main.go   # Run development server
go build         # Build executable
```

## 🌐 Production Deployment

### Environment Variables
Ensure all production environment variables are properly configured:
- Database connection details
- JWT secret keys
- CORS origins
- SSL certificate paths

### SSL/HTTPS
The application is configured to support HTTPS with Let's Encrypt certificates. Update the SSL certificate paths in `server/main.go` for production.

### Performance Optimization
- Enable Astro's built-in optimizations
- Configure database connection pooling
- Set up CDN for static assets
- Implement caching strategies

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in the GitHub repository
- Check the documentation in the `/docs` folder
- Review the API endpoints documentation

## 🔮 Roadmap

- [ ] User profile management
- [ ] Comment system
- [ ] Social media integration
- [ ] Advanced search functionality
- [ ] Analytics dashboard
- [ ] Multi-language support
- [ ] Mobile app development

---

**Built with ❤️ using Astro and Go** 
