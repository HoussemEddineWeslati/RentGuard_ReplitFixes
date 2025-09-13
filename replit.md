# Overview

This is a comprehensive GLI (Gestion des Loyers Impayés) web application designed to help landlords protect their rental income through automated rent tracking and insurance premium calculations. The application provides landlords with tools to manage properties and tenants, track payment statuses, calculate insurance premiums, and subscribe to different service plans.

The system operates as a SaaS platform with multiple subscription tiers (Free, Pro, Enterprise) and includes features for property management, tenant tracking, automated rent monitoring, and GLI insurance quote generation.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **React with TypeScript**: Modern React application using functional components and hooks
- **Wouter**: Lightweight client-side routing solution for navigation between pages
- **TanStack Query**: Server state management for API calls, caching, and synchronization
- **React Hook Form + Zod**: Form handling with schema validation for type safety
- **Tailwind CSS + shadcn/ui**: Utility-first styling with pre-built component library
- **Vite**: Build tool and development server for fast development experience

## Backend Architecture
- **Express.js with TypeScript**: RESTful API server with type safety
- **Session-based Authentication**: Express sessions with bcrypt password hashing
- **Memory Storage**: In-memory data storage for development/demo purposes
- **Drizzle ORM**: Type-safe database ORM configured for PostgreSQL (ready for production)
- **Modular Route Structure**: Organized API endpoints for auth, properties, tenants, quotes, and subscriptions

## Data Layer Design
- **Shared Schema**: Common TypeScript types and Zod schemas between frontend and backend
- **Relational Data Model**: Users -> Properties -> Tenants with proper foreign key relationships
- **Quote System**: Standalone quote calculations with user association
- **Subscription Management**: Plan-based access control with different feature tiers

## Authentication & Authorization
- **Session-based Auth**: Server-side sessions with secure cookie handling
- **Route Protection**: Middleware-based authentication checking for protected endpoints
- **Client-side Auth State**: React Query-powered authentication state management
- **Password Security**: bcrypt hashing for secure password storage

## Key Features Implementation
- **Property Management**: Full CRUD operations for rental properties
- **Tenant Tracking**: Payment status monitoring with automated overdue detection
- **Premium Calculator**: Dynamic GLI insurance quote generation based on risk factors
- **Dashboard Analytics**: Real-time metrics showing tenant status, unpaid rents, and financial overview
- **Subscription Plans**: Tiered access system with feature limitations based on plan level

# External Dependencies

## Core Framework Dependencies
- **React Ecosystem**: React 18 with TypeScript, React Router (Wouter), React Hook Form
- **UI Components**: Radix UI primitives with shadcn/ui component library
- **Styling**: Tailwind CSS with PostCSS for utility-first styling
- **Build Tools**: Vite for development and production builds, ESBuild for server bundling

## Backend Dependencies
- **Express.js**: Web framework with session middleware and security utilities
- **Database**: Drizzle ORM configured for PostgreSQL with Neon Database serverless driver
- **Authentication**: bcrypt for password hashing, express-session for session management
- **Development**: tsx for TypeScript execution, nodemon-style development workflow

## Development & Deployment
- **TypeScript**: Full type safety across frontend, backend, and shared schemas
- **Replit Integration**: Configured with Replit-specific plugins and development tools
- **Session Storage**: Memory-based session store for development, extensible to Redis/PostgreSQL for production
- **Environment Configuration**: Environment-based configuration for database connections and secrets

## Database Configuration
- **PostgreSQL Ready**: Drizzle configuration points to PostgreSQL with proper migrations setup
- **Schema Management**: Centralized schema definitions with automatic type generation
- **Migration System**: Database migration support through Drizzle Kit
- **Development Fallback**: In-memory storage implementation for development without database setup