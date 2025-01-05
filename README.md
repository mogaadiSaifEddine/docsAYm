# Soar Financial Dashboard Documentation

## Overview
This documentation outlines the development and deployment process of the Soar financial dashboard project, a Next.js-based web application for financial data visualization and management.

- **Author**: Aymen KHEDHRIYA
- **Repository**: [GitHub](https://github.com/AymKh/soar-dashboard/)
- **Live Demo**: [https://soar.maak-corp.tn/](https://soar.maak-corp.tn/)

## Development Environment

### Technology Stack
- **Framework**: Next.js 15
- **Styling**: TailwindCSS
- **Code Quality**: Prettier, ESLint
- **Monitoring**: Sentry

### Initial Setup
1. Created a new Next.js 15 project
2. Configured development tools:
   - Prettier for consistent code formatting across team
   - ESLint for real-time error detection
   - TailwindCSS configuration with custom theme variables
3. Set up Sentry for production monitoring and error tracking

### Architectural Decisions

#### Routing Implementation
While the assignment specified using react-router-dom, we opted for Next.js's built-in routing system due to:
- Better integration with Next.js features
- Enhanced performance optimization
- Server-side rendering capabilities
- Built-in API route handling

## Development Workflow

### Git Strategy
Implemented a simplified git flow with three main branches:

```
main (production) 
  ↑
develop (milestone features)
  ↑
feature branches (individual features)
```

#### Branch Purposes
- **main**: Production-ready code, deployed to Vercel
- **develop**: Integration branch for feature completion
- **feature branches**: Individual feature development

### Development Phases

#### Phase 1: Layout Implementation
Completed through two main pull requests:
1. [Initial Layout Structure](https://github.com/AymKh/soar-dashboard/pull/1)
2. [Layout Refinements](https://github.com/AymKh/soar-dashboard/pull/2)

#### Phase 2: Component Development
- Components organized under `/app/components`
- Dashboard view constructed at root route ("/)
- Responsive design implemented using:
  - Grid layouts
  - Flexbox
  - TailwindCSS utilities

## Backend Architecture

### API Implementation
Chose Next.js route handlers over traditional 3-tier architecture for:
- Improved security
- Better integration with Next.js
- Simplified deployment
- Reduced infrastructure complexity

#### Current Implementation
- Created route handler for cards at `/app/mock/cards/route.ts`
- Implemented GET endpoint with mock data
- Added loading state handling

### Potential Full Architecture
For future scaling, could implement full 3-tier architecture:
```
Frontend (Next.js) → API (NestJS) → Database
```

Deployment options:
- DigitalOcean
- Vercel
- Netlify

## Monitoring and Quality Assurance

### Error Tracking
- Integrated Sentry for production monitoring
- Tracks runtime errors and performance metrics
- Provides real-time error reporting and analytics

### Future Improvements
1. Implement additional API endpoints for:
   - Contact list
   - Transaction history
   - User authentication
2. Add comprehensive error handling
3. Implement proper loading states and animations
4. Expand test coverage
5. Set up CI/CD pipeline

## Project Structure
```
/app
  /components     # Reusable UI components
  /mock          # Mock API routes
    /cards
      route.ts   # Cards API handler
      loading.ts # Loading state
  /styles        # Global styles
tailwind.config.ts # TailwindCSS configuration
```
