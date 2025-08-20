# Simple React Folder

A powerful VSCode extension designed to streamline the creation of Next.js pages and React components. Boost your development productivity with one-click folder generation and intelligent templates.

## Why Use Simple React Folder?

Creating React components and Next.js pages manually can be time-consuming and repetitive. This extension eliminates the boilerplate work by:

- **Instant Setup**: Create complete component/page structures in seconds
- **Next.js Ready**: Pre-configured templates with `getServerSideProps` for pages
- **TypeScript First**: Built-in TypeScript support with proper interfaces
- **CSS Modules**: Automatic CSS module file generation with your preferred preprocessor
- **Consistent Structure**: Maintains uniform folder organization across your project

## Features

- 🚀 **Lightning Fast**: Right-click to create components and pages instantly
- 📁 **Smart Templates**: Pre-built templates for both components and Next.js pages
- 🎨 **Flexible Styling**: Support for SCSS, CSS, Less, and Sass with CSS modules
- ⚡ **Intelligent Naming**: Automatic file and class naming based on your input
- 🔧 **Developer Experience**: Auto-reveal in explorer with rename support
- ⚙️ **Customizable**: Configure your preferred style file extension
- 📄 **Next.js Optimized**: Page templates include `getServerSideProps` and proper exports

## Quick Start

### Create a React Component

1. Right-click in your project folder
2. Select "Create Component"
3. Enter component name (e.g., `UserCard`)
4. Done! Your component is ready to use

### Create a Next.js Page

1. Right-click in your `pages` directory
2. Select "Create Page"
3. Enter page name (e.g., `dashboard`)
4. Done! Your page includes `getServerSideProps` and is ready for routing

## Generated Structure

### Component Structure
```
UserCard/
├── index.tsx          # Component with TypeScript interface
└── index.module.scss  # CSS module file
```

### Page Structure
```
dashboard/
├── index.tsx          # Next.js page with getServerSideProps
└── index.module.scss  # CSS module file
```

## Template Examples

### React Component Template
```tsx
import React from 'react';
import Style from './index.module.scss';

interface UserCardProps {
    // define your props here
}

const UserCard: React.FC<UserCardProps> = () => {
    return (
        <div className={Style.UserCard}>
            UserCard Component
        </div>
    );
};

export default UserCard;
```

### Next.js Page Template
```tsx
import React from 'react';
import type { GetServerSideProps } from 'next';
import Style from './index.module.scss';

interface IDashboardProps {
    // define your props here
}

const Dashboard: React.FC<IDashboardProps> = () => {
    return (
        <div className={Style.Dashboard}>
            <h1>Dashboard</h1>
            <p>This is the Dashboard page</p>
        </div>
    );
};

export const getServerSideProps: GetServerSideProps = async (ctx) => {
    // Add your server-side logic here
    return {
        props: {
            xdata: null,
        },
    };
};

export default Dashboard;
```

## Configuration

### Style File Extension

Customize your preferred CSS preprocessor in VSCode settings:

1. Open Settings (`Ctrl+,` or `Cmd+,`)
2. Search "Simple React Folder"
3. Set "Style File Extension" to your preference:
   - `.scss` (default)
   - `.css`
   - `.less`
   - `.sass`

### Via settings.json
```json
{
  "simpleReactFolder.styleFileExtension": ".css"
}
```

## Usage Methods

### Method 1: Right-click Menu
- Navigate to your target folder
- Right-click and select "Create Component" or "Create Page"
- Enter the name and press Enter

### Method 2: Command Palette
- Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
- Type "Create Component" or "Create Page"
- Select the command and enter the name

## Perfect for Next.js Projects

This extension is specifically designed for Next.js development:

- **Pages Directory**: Create pages that work seamlessly with Next.js routing
- **Server-Side Rendering**: Templates include `getServerSideProps` for SSR
- **TypeScript Support**: Full TypeScript integration with proper type definitions
- **CSS Modules**: Built-in CSS module support for scoped styling
- **File-based Routing**: Generated pages automatically work with Next.js file-based routing

## Development Workflow

1. **Create Component**: Use for reusable UI components
2. **Create Page**: Use for Next.js pages in your `pages` directory
3. **Customize**: Modify the generated templates to fit your needs
4. **Style**: Add your CSS/SCSS styles in the generated module file
5. **Export**: Components and pages are ready to import and use

## System Requirements

- VSCode 1.80.0 or higher
- Node.js 16.0.0 or higher (for development)

## Development

### Local Setup
```bash
git clone https://github.com/kkk360/simple-react-folder
cd simple-react-folder
npm install
npm run compile
# Press F5 in VSCode to start debugging
```

### Build
```bash
npm run package  # Build extension
npm run publish  # Publish to marketplace
```

## License

MIT License

## Contributing

Issues and Pull Requests are welcome!

## Changelog

### v0.0.5
- Added "Create Page" command with Next.js `getServerSideProps` support
- Enhanced page templates for better Next.js integration
- Improved TypeScript interface naming conventions
- Added right-click menu support for page creation

### v0.0.4
- Added configuration for custom style file extensions
- Support for multiple CSS preprocessors (.scss, .css, .less, .sass)
- Optimized file generation and template system

### v0.0.3
- Initial release with React component creation
- TypeScript and SCSS template generation

## Author

wangxiaohai

## Repository

https://github.com/kkk360/simple-react-folder
