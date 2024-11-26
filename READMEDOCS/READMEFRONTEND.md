# Frontend Documentation

## Table of Contents
1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Core Technologies](#core-technologies)
4. [Configuration Files](#configuration-files)
5. [Main Application](#main-application)
6. [Components](#components)
7. [Backend Integration](#backend-integration)
8. [Authentication](#authentication)
9. [Styling](#styling)
10. [State Management](#state-management)

## Overview

This frontend application is a React-based video analysis chatbot that allows users to:
- Upload and analyze video content
- Chat with an AI assistant about video analysis
- Track chat and video analysis history
- Manage user authentication
- View detailed analytics and insights

The application uses a modern tech stack with TypeScript, Tailwind CSS, and shadcn/ui components, featuring a glass-morphism design aesthetic.

## Project Structure

frontend/
├── src/
│ ├── components/
│ │ ├── chat/
│ │ ├── home/
│ │ └── ui/
│ ├── context/
│ ├── lib/
│ ├── types/
│ ├── App.tsx
│ └── main.tsx
├── public/
├── components.json
├── index.html
├── jsconfig.json
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.ts



## Core Technologies

- **React**: v18.2.0
- **TypeScript**: v5.3.3
- **Vite**: v5.0.6
- **Tailwind CSS**: v3.3.6
- **shadcn/ui**: Custom components
- **Radix UI**: Primitive components
- **Lucide React**: Icon system
- **React Router DOM**: v6.20.1

## Configuration Files

### components.json

json
{
"style": "default",
"rsc": false,
"tsx": true,
"tailwind": {
"config": "tailwind.config.js",
"css": "src/index.css",
"baseColor": "slate",
"cssVariables": true
}

Configures shadcn/ui components and their styling preferences.

### jsconfig.json
Enables path aliases for cleaner imports:

json
{
"compilerOptions": {
"baseUrl": ".",
"paths": {
"@/": ["./src/"]
}
}
}


### package.json
Contains all dependencies and scripts:
- `dev`: Runs development server
- `build`: Builds production bundle
- `preview`: Previews production build
- `typecheck`: Runs TypeScript type checking

## Main Application

### App.tsx
The root component managing:
- Chat history state
- Video history state
- Current chat session
- Error handling
- Layout structure

Key features:
- Sidebar navigation
- Chat container
- History tracking
- Real-time updates

## Components

### Chat Components

#### ChatContainer.tsx
Main chat interface handling:
- Message sending/receiving
- File uploads
- Real-time chat updates
- Error handling
- Drag-and-drop functionality

Features:
- Multi-file upload support
- Progress tracking
- Message history
- Loading states
- Error feedback

#### ChatHeader.tsx
Displays:
- Window controls (red, yellow, green dots)
- Progress indicators
- Navigation breadcrumbs

#### ChatInput.tsx
Handles:
- Message input
- Send functionality
- Loading states
- Input validation

#### ChatMessage.tsx
Renders individual messages with:
- User/bot differentiation
- Timestamps
- Avatar display
- Message styling

#### ChatWelcome.tsx
Initial chat screen showing:
- Welcome message
- Getting started instructions
- Brand elements

### Home Components

#### CompanySlider.tsx
Animated company logo slider:
- Continuous scroll
- Responsive design
- Brand showcase

#### DemoSection.tsx
Showcases:
- Demo booking
- Pricing tiers
- Enterprise features

#### FeatureCard.tsx
Displays individual features with:
- Icon
- Title
- Description
- Hover effects

#### GlassCard.tsx
Reusable component providing:
- Glass morphism effect
- Border styling
- Background blur
- Hover states

#### MetricsBanner.tsx
Interactive metrics display:
- Auto-rotating use cases
- Progress indicators
- Manual selection
- Image transitions

#### ModelCard.tsx
Displays AI model information:
- Model name
- Size
- Type
- Visual indicators

#### Navbar.tsx
Navigation component with:
- Authentication links
- Main navigation
- Responsive design
- Glass effect

#### RotatingText.tsx
Animated text display:
- Auto-rotating messages
- Smooth transitions
- Configurable timing

#### SearchBar.tsx
Search functionality with:
- Glass morphism design
- Icon integration
- Placeholder text
- Focus states

### Authentication Components

#### LoginForm.tsx
Handles user authentication:
- Email/password inputs
- Form validation
- Error handling
- Redirect logic
- Loading states

#### ProtectedRoute.tsx
Route protection with:
- Authentication checking
- Loading states
- Redirect handling
- State preservation

## Backend Integration

The frontend communicates with the backend through several endpoints:

### Chat Endpoints
- `/send_message`: Sends chat messages and video uploads
- `/chat_history`: Retrieves chat history
- `/video_analysis_history`: Retrieves video analysis history

### Authentication Endpoints
- `/login`: User authentication
- `/logout`: Session termination

## Authentication

Authentication is managed through:
- Protected routes
- Session management
- Login/logout functionality
- Redirect handling
- State persistence

## Styling

### Design System
- Glass morphism effects
- Consistent color palette
- Responsive design
- Dark mode support

### Tailwind Configuration
- Custom colors
- Animation utilities
- Responsive breakpoints
- Component variants

### Component Styling
- Consistent spacing
- Typography system
- Interactive states
- Accessibility considerations

## State Management

### Global State
- User authentication
- Current chat session
- Error handling

### Local State
- Form inputs
- Loading states
- UI interactions
- File uploads

### Context Usage
- Authentication context
- Theme context
- Chat context

## Performance Considerations

### Optimizations
- Lazy loading
- Image optimization
- Code splitting
- Memoization

### Error Handling
- Form validation
- API error handling
- Fallback UI
- Error boundaries

## Development Guidelines

### Best Practices
- TypeScript strict mode
- Component composition
- Props validation
- Error boundaries
- Performance monitoring

### Code Style
- Consistent naming
- Component organization
- Type definitions
- Documentation

This documentation provides a comprehensive overview of the frontend application, its structure, and functionality. It serves as a complete reference for developers working with the codebase, whether they're new to the project or maintaining existing features.