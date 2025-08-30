# Overview

EduBridgeAI is a comprehensive AI-powered education platform that provides personalized tutoring, content creation, and assessment tools. The application features an interactive AI tutor for real-time learning assistance, content creation tools for educators, quiz builders with adaptive questioning, and analytics dashboards for tracking learning progress. Built as a full-stack TypeScript application, it combines modern web technologies with AI services to deliver an engaging educational experience.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The client-side is built with React and TypeScript using Vite as the build tool. The application follows a component-based architecture with:
- **UI Framework**: Radix UI primitives with shadcn/ui components for consistent, accessible design
- **Styling**: Tailwind CSS with custom CSS variables for theming support
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query for server state management and data fetching
- **Form Handling**: React Hook Form with Zod validation for type-safe forms

## Backend Architecture
The server runs on Express.js with TypeScript, implementing a RESTful API design:
- **Runtime**: Node.js with ESM modules
- **Framework**: Express.js for HTTP server and middleware
- **API Design**: RESTful endpoints with standardized response formats
- **Error Handling**: Centralized error middleware with proper HTTP status codes
- **Development**: Hot reloading with Vite middleware integration

## Database Layer
Data persistence is handled through Drizzle ORM with PostgreSQL:
- **ORM**: Drizzle ORM for type-safe database operations and migrations
- **Database**: PostgreSQL with Neon serverless database hosting
- **Schema Management**: Shared schema definitions between client and server
- **Migration System**: Drizzle Kit for database schema migrations

The database schema supports educational entities including users, chat sessions, messages, quizzes, quiz attempts, and educational content with proper relationships and constraints.

## AI Integration
AI capabilities are powered by OpenAI's GPT models:
- **Model**: GPT-5 for advanced language understanding and generation
- **Use Cases**: Conversational tutoring, content generation, quiz creation, and explanation generation
- **Context Management**: Conversation history tracking for coherent multi-turn interactions
- **Subject Specialization**: Context-aware responses based on educational subjects

## Authentication & Session Management
User authentication uses a simplified approach for the current implementation:
- **Demo User System**: Currently uses a demo user ("demo-user-1") for development
- **Session Storage**: PostgreSQL-based session storage with connect-pg-simple
- **Future-Ready**: Architecture supports full authentication system integration

# External Dependencies

## Core Technologies
- **React 18**: Component-based UI framework with modern hooks
- **TypeScript**: Type safety across the entire application stack
- **Vite**: Fast build tool and development server
- **Express.js**: Web application framework for Node.js

## Database & ORM
- **Drizzle ORM**: Modern TypeScript ORM for database operations
- **PostgreSQL**: Primary database with Neon serverless hosting
- **@neondatabase/serverless**: Serverless PostgreSQL driver

## AI Services
- **OpenAI API**: GPT-5 model for AI-powered educational features
- **Custom AI Service Layer**: Abstraction for different AI use cases (tutoring, content generation, quiz creation)

## UI & Styling
- **Radix UI**: Accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework
- **shadcn/ui**: Pre-built component library with design system
- **Lucide React**: Icon library for consistent iconography

## Development Tools
- **Replit Integration**: Development environment with runtime error overlay
- **PostCSS**: CSS processing with Autoprefixer
- **ESBuild**: Fast JavaScript bundler for production builds

## Data Fetching & Forms
- **TanStack Query**: Server state management and caching
- **React Hook Form**: Form state management and validation
- **Zod**: Schema validation for type safety

## Additional Libraries
- **date-fns**: Date manipulation and formatting
- **class-variance-authority**: Component variant styling
- **wouter**: Lightweight client-side routing
- **embla-carousel**: Carousel/slider component functionality