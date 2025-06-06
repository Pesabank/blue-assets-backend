# BlueAssets Backend

Enterprise-grade asset management API built with Node.js, Express, TypeScript, and Prisma.

## Quick Start

```bash
# Install dependencies
npm install

# Copy environment file
cp .env.example .env
# Edit .env with your values

# Setup database
npx prisma generate
npx prisma db push
npm run seed

# Start development server
npm run dev
```

## Features

- **Authentication & Authorization**: JWT-based auth with role-based access control
- **Asset Management**: Complete CRUD operations for assets, assignments, and tracking
- **Request Management**: Employee asset requests with approval workflow
- **Maintenance Scheduling**: Preventive and corrective maintenance tracking
- **Real-time Notifications**: WebSocket support for live updates
- **Background Jobs**: Automated reminders and maintenance checks
- **Audit Logging**: Complete activity tracking for compliance
- **Multi-tenant**: Organization-based data separation

## API Endpoints

### Authentication
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/logout` - User logout
- `GET /api/v1/auth/me` - Get current user

### Admin
- `GET /api/v1/admin/assets` - List assets
- `POST /api/v1/admin/assets` - Create asset
- `PUT /api/v1/admin/assets/:id` - Update asset
- `DELETE /api/v1/admin/assets/:id` - Delete asset

### Employee
- `GET /api/v1/employee/my-assets` - Get my assigned assets
- `POST /api/v1/employee/asset-requests` - Create asset request
- `GET /api/v1/employee/asset-history` - View asset history

## Default Users (after seeding)

- **SuperAdmin**: `superadmin@blueassets.com` / `superadmin123`
- **Admin**: `admin@acme.com` / `admin123`
- **Employee**: `employee@acme.com` / `employee123`

## Technology Stack

- **Runtime**: Node.js 18+
- **Framework**: Express.js with TypeScript
- **Database**: SQLite (dev) / PostgreSQL (production)
- **ORM**: Prisma
- **Authentication**: JWT
- **Real-time**: Socket.io
- **Jobs**: Bull with Redis
- **Logging**: Winston

## Development Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run test` - Run tests
- `npm run seed` - Seed database with sample data

## License

MIT License - see LICENSE file for details.
