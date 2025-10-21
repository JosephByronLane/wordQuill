# WordQuill Frontend Structure

This is the Angular frontend for wordQuill, a web-based text editor for writing stories and creating worlds.

## Folder Structure

```
src/
├── app/
│   ├── core/                    # Core module (singleton services, guards, interceptors)
│   │   ├── guards/              # Route guards
│   │   ├── interceptors/        # HTTP interceptors
│   │   └── services/            # Core singleton services (auth, API, etc.)
│   │
│   ├── features/                # Feature modules
│   │   ├── auth/                # Authentication module
│   │   │   └── components/      # Login, register, forgot-password
│   │   │
│   │   ├── stories/             # Stories management module
│   │   │   └── components/      # Story list, story card, etc.
│   │   │
│   │   ├── editor/              # Main text editor module
│   │   │   ├── components/      # Editor UI components
│   │   │   └── services/        # Editor-specific services
│   │   │
│   │   ├── world/               # World-building module
│   │   │   ├── components/      # Character, item, kingdom entries
│   │   │   └── models/          # World entity models
│   │   │
│   │   └── settings/            # User settings module
│   │       └── components/      # Settings pages
│   │
│   ├── shared/                  # Shared module
│   │   ├── components/          # Reusable components
│   │   │   ├── sidebar/         # Sidebar component for world entries
│   │   │   ├── modal/           # Modal component
│   │   │   ├── comments/        # Comments component
│   │   │   ├── header/          # App header
│   │   │   └── footer/          # App footer
│   │   ├── directives/          # Shared directives
│   │   └── pipes/               # Shared pipes
│   │
│   └── models/                  # Global TypeScript interfaces and types
│
├── assets/                      # Static assets
│   ├── images/                  # Images and icons
│   ├── styles/                  # Global stylesheets
│   └── fonts/                   # Custom fonts
│
└── environments/                # Environment configurations
    ├── environment.ts           # Development environment
    └── environment.prod.ts      # Production environment
```

## Key Features

### Pages
- **Login Screen** (`features/auth/components`)
- **Your Stories** (`features/stories/components`)
- **Text Editor** (`features/editor/components`)

### UI Components
- **Sidebar** (`shared/components/sidebar`) - For world entries (characters, items, kingdoms)
- **Comments** (`shared/components/comments`) - For text editing page
- **Modal Panes** (`shared/components/modal`) - For various modal dialogs
- **Settings** (`features/settings/components`) - User settings

### Core Services
- Authentication
- API communication
- State management
