# Recommendo - AI-Powered Recommendation System

## Overview

Recommendo is a comprehensive recommendation platform that provides personalized suggestions for movies, music, and products. The system employs multiple recommendation algorithms including collaborative filtering, content-based filtering, and hybrid approaches to deliver accurate recommendations. Built with a modern React frontend and Express.js backend, it features real-time analytics, user feedback collection, and an integrated AI chatbot for enhanced user interaction.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript and Vite for build tooling
- **UI Library**: Shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design system including dark/light theme support
- **State Management**: TanStack Query for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Charts**: Chart.js for analytics visualization

The frontend follows a component-based architecture with reusable UI components, custom hooks for functionality like mobile detection and theming, and a centralized query client for API communication.

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **API Design**: RESTful endpoints for user management, recommendations, ratings, and feedback
- **Development Server**: Custom Vite integration for hot reloading in development
- **Request Logging**: Comprehensive middleware for API request/response logging
- **Error Handling**: Centralized error handling with proper status codes

The backend uses a modular structure with separate route handlers and service layers for different functionalities.

### Database Layer
- **ORM**: Drizzle ORM for type-safe database operations
- **Database**: PostgreSQL with Neon Database serverless driver
- **Schema**: Well-defined tables for users, items, ratings, recommendations, and feedback
- **Migrations**: Drizzle Kit for database schema management

The database schema supports multiple item types (movies, music, products) with flexible JSON fields for metadata and features.

### Recommendation Engine
- **Algorithms**: Multiple recommendation strategies implemented:
  - Collaborative filtering (user-based similarity)
  - Content-based filtering (item features and genres)
  - Hybrid approach combining multiple methods
- **Storage Interface**: Abstracted storage layer with in-memory implementation for development
- **Scoring System**: Confidence scores for recommendation quality assessment

### AI Integration
- **Chatbot Service**: OpenAI GPT-5 integration for conversational recommendations
- **Context Awareness**: User history and preferences integrated into AI responses
- **Structured Responses**: JSON-formatted responses for consistent UI integration

### Session Management
- **Session Storage**: PostgreSQL session store using connect-pg-simple
- **User Context**: Persistent user sessions across requests

## External Dependencies

### Core Infrastructure
- **Database**: Neon Database (PostgreSQL serverless)
- **AI Service**: OpenAI API for chatbot functionality

### Frontend Libraries
- **UI Components**: Radix UI primitives for accessible components
- **Styling**: Tailwind CSS for utility-first styling
- **State Management**: TanStack React Query for server state
- **Charts**: Chart.js for data visualization
- **Date Handling**: date-fns for date manipulation
- **Form Handling**: React Hook Form with Zod validation

### Backend Libraries
- **Database**: Drizzle ORM with PostgreSQL driver
- **Session Management**: express-session with PostgreSQL store
- **Validation**: Zod for runtime type validation
- **Development**: tsx for TypeScript execution, esbuild for production builds

### Development Tools
- **Build System**: Vite with React plugin
- **Replit Integration**: Cartographer plugin and runtime error overlay
- **Type Checking**: TypeScript with strict configuration
- **Code Quality**: Path aliases for clean imports

The system is designed to be scalable and maintainable, with clear separation of concerns between the frontend, backend, and external services.