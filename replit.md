# LdrLog - Leadership Development Platform

## Overview

LdrLog is a full-stack web application designed for professional leadership development across various industries including healthcare, education, business, military, technology, and non-profit sectors. The platform enables users to log events that develop leadership competencies through real-world experience tracking.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **UI Library**: Shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter for lightweight client-side routing
- **Animations**: Framer Motion for interactive animations
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with TypeScript
- **Framework**: Express.js for REST API endpoints
- **Database ORM**: Drizzle ORM with PostgreSQL dialect
- **Database**: Configured for Neon Database (serverless PostgreSQL)
- **Session Management**: PostgreSQL-based sessions with connect-pg-simple
- **Build System**: Vite for frontend, esbuild for backend bundling

### Development Setup
- **Monorepo Structure**: Shared types and schemas between client/server
- **Hot Reload**: Vite dev server with HMR integration
- **Type Safety**: Full TypeScript coverage with strict configuration
- **Code Quality**: ESLint integration with shadcn/ui standards

## Key Components

### Database Schema (`shared/schema.ts`)
- **Users Table**: Basic user authentication with username/password
- **Drizzle Integration**: Type-safe schema definitions with Zod validation
- **Migration Support**: Automated migrations through drizzle-kit

### Storage Layer (`server/storage.ts`)
- **Abstraction**: IStorage interface for database operations
- **Memory Implementation**: In-memory storage for development/testing
- **CRUD Operations**: User management with create, read operations
- **Extensible Design**: Easy to add new entities and operations

### UI Components
- **Design System**: Comprehensive component library with consistent theming
- **Accessibility**: ARIA-compliant components from Radix UI
- **Responsive**: Mobile-first design with breakpoint utilities
- **Dark Mode**: CSS variable-based theming system

### API Structure
- **RESTful Design**: Express routes with `/api` prefix
- **Error Handling**: Centralized error middleware
- **Request Logging**: Automatic API request/response logging
- **Type Safety**: Shared types between frontend and backend

## Data Flow

1. **Client Requests**: React components use TanStack Query for API calls
2. **API Layer**: Express routes handle HTTP requests with validation
3. **Storage Layer**: Storage interface abstracts database operations
4. **Database**: PostgreSQL with Drizzle ORM for type-safe queries
5. **Response**: JSON responses with proper error handling

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Serverless PostgreSQL connection
- **drizzle-orm**: Type-safe database toolkit
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI component primitives
- **tailwindcss**: Utility-first CSS framework
- **wouter**: Lightweight React router

### Development Dependencies
- **vite**: Fast build tool and dev server
- **tsx**: TypeScript execution for development
- **esbuild**: Fast JavaScript bundler for production
- **@replit/vite-plugin-***: Replit-specific development tools

## Deployment Strategy

### Production Build
- **Frontend**: Vite builds optimized React bundle to `dist/public`
- **Backend**: esbuild bundles Express server to `dist/index.js`
- **Assets**: Static files served through Express in production

### Environment Configuration
- **DATABASE_URL**: Required PostgreSQL connection string
- **NODE_ENV**: Environment detection for development/production modes
- **Session Configuration**: PostgreSQL-backed sessions for scalability

### Scaling Considerations
- **Database**: Serverless PostgreSQL supports automatic scaling
- **Static Assets**: Can be moved to CDN for better performance
- **API**: Express server can be containerized and horizontally scaled

## Changelog

```
Changelog:
- July 05, 2025. Initial setup
- July 05, 2025. Updated with 8 specific Leader Log applications using branded logos:
  * Healthcare Leader Log
  * Educator Leader Log  
  * Corporate Leader Log
  * First Responder Leader Log
  * Entrepreneur/Startup Leader Log
  * Nonprofit Leader Log
  * Government Leader Log
  * Coach & Mentor Leader Log
- July 05, 2025. Added Military Leader Log (9th application) with branded logo, maintaining alphabetical order
- July 05, 2025. Connected Military Leader Log to live application at https://military-leader-log.replit.app/
- July 05, 2025. Improved text readability by removing text shadows and gray backgrounds
- July 05, 2025. Changed hero text from white to black for better contrast and readability
- July 05, 2025. Updated messaging from "revolutionizes" to "improves" per user preference
- July 05, 2025. Added comprehensive copyright notice to footer with Tom Hong copyright and legal disclaimer
- July 05, 2025. Added "Created by Tom Hong" link to tomhong.com in footer
- July 05, 2025. Removed "Schedule a Demo" button and made CTA section text black on white background
- July 05, 2025. Updated contact email from contact@ldrlog.com to tomhong2030@gmail.com
- July 05, 2025. Updated contact address to PSC 400 Box 1694, APO AP 96273
- July 05, 2025. Reordered Professional Tools list in footer to alphabetical order
- July 05, 2025. Changed all "methodology" references to "Features" throughout the website
- July 05, 2025. Updated statistic from "500+ Leaders Developed" to "1 Leader Developed"
- July 05, 2025. Updated "12 Industries Served" to "9 Industries Served" to match actual profession count
- July 05, 2025. Added "Other Leader Log" (10th application) with "Coming Soon" functionality using branded logo
- July 05, 2025. Updated phone number to "800-coming-soon"
- July 05, 2025. Updated brand orange color to RGB(215, 118, 54) for all orange elements
- July 05, 2025. Replaced testimonials section with "Seeking Testimonies from Beta Users" using User icons instead of photos
- July 05, 2025. Added "Future App" stickers to all Leader Log applications except Military Leader Log (the only deployed app)
- July 05, 2025. Updated tagline to include "profession" alongside "industry" for more comprehensive messaging
- July 05, 2025. Optimized website for mobile devices with responsive typography, layouts, and spacing
- July 05, 2025. Reduced floating "9 Leader Log Apps" tile size by 2x to prevent overlap with main logo
- July 05, 2025. Moved "9 Leader Log Apps" from floating position to top of "Leadership Tools for Every Profession" section
- July 05, 2025. Created comprehensive "App Features" page (/features) with content from elevator pitch documents
- July 05, 2025. Removed contact form functionality, enhanced contact section with custom app development messaging
- July 05, 2025. Added navigation link from "Learn about App Features" button to new features page
- July 05, 2025. Added LDRLOG logo to features page header with professional layout design
- July 05, 2025. Created "Get Started" page (/get-started) using provided copy with 6-step onboarding process
- July 05, 2025. Connected "Get Started Today" button from homepage to new get-started page
- July 05, 2025. Updated top navigation menu "Get Started" buttons (desktop and mobile) to link to new get-started page
- July 05, 2025. Updated all orange color elements across all pages to use brand RGB(215, 118, 54) with consistent hover effects
- July 05, 2025. Fixed visibility issues on features and get-started pages by making transparent text visible and improving icon contrast
- July 05, 2025. Fixed gradient rendering issues causing white icons to appear invisible by replacing single-color gradients with solid backgrounds
- July 05, 2025. Optimized get-started page for mobile devices with responsive typography, layouts, and spacing for optimal mobile viewing experience
- July 05, 2025. Fixed icon centering in get-started page - all icons now properly centered within their outline shapes for mobile devices
- July 05, 2025. Fixed icon centering in features page - hero Brain icon, statistics icons, and feature card icons now properly centered within outline shapes for mobile devices
- July 05, 2025. Fixed mobile navigation scroll issue - added ScrollToTop component to ensure users are taken to top of pages when navigating, especially on mobile devices
- July 05, 2025. Enhanced scroll-to-top functionality with aggressive mobile compatibility - added multiple scroll methods, timing delays, and requestAnimationFrame for reliable mobile performance across all pages
- July 05, 2025. Reordered leadership apps to prioritize Military Leader Log as first app (only deployed application) followed by others in alphabetical order
- July 05, 2025. Added LDRS1toN company family branding to all page footers with prominent logo placement and "Part of the LDRS1toN Company Family of Apps" messaging
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```