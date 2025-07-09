# Getting Started: Building PropertyFlow with Cursor

## Quick Start Guide

### Step 1: Initial Setup
1. **Open a new Cursor window** and create a new folder for your project
2. **Open the folder in Cursor** - this will be your workspace
3. **Use Cursor's AI chat** (Cmd/Ctrl + L) and paste this prompt:

```
Create a production-ready UK property management system called PropertyFlow with the following tech stack:

- Monorepo structure with separate tenant/landlord frontends
- Backend: TypeScript + Express.js + PostgreSQL + Drizzle ORM
- Frontend: React + TypeScript + Shadcn/UI + Tailwind CSS
- Authentication: Role-based access for tenants/landlords
- Payment: Open Banking integration + Stripe/GoCardless
- Document management: Secure file upload and storage
- UK compliance: Right to Rent verification, GDPR, safety certificates

Please start by creating the project structure and package.json files.
```

### Step 2: Project Structure Creation
Ask Cursor to create this structure:
```
propertyflow/
├── apps/
│   ├── landlord-portal/     # Landlord React app
│   ├── tenant-portal/       # Tenant React app
│   └── api/                 # Express.js backend
├── packages/
│   ├── ui/                  # Shared UI components
│   ├── database/            # Drizzle schema & migrations
│   └── types/               # Shared TypeScript types
├── package.json
└── README.md
```

### Step 3: Progressive Development Prompts

#### Phase 1: Core Infrastructure
```
Set up the backend API with:
1. Express.js server with TypeScript
2. PostgreSQL database connection
3. Drizzle ORM setup with basic schemas for:
   - Users (landlords/tenants)
   - Properties (UK address structure)
   - Documents
   - Payments
4. Basic authentication middleware
5. Environment configuration
```

#### Phase 2: Database Schema
```
Create comprehensive Drizzle schemas for UK property management:
1. Properties table (address, postcode validation, property types)
2. Users table (role-based: landlord/tenant)
3. Tenancies table (linking properties to tenants)
4. Documents table (secure file storage, compliance tracking)
5. Payments table (Open Banking integration fields)
6. Maintenance requests table
7. Communications table

Include UK-specific validations (postcodes, property types, Right to Rent fields).
```

#### Phase 3: Frontend Setup
```
Create the landlord portal with:
1. React + TypeScript + Vite setup
2. Shadcn/UI components installation
3. Tailwind CSS configuration
4. Authentication pages (login/signup)
5. Dashboard layout with sidebar navigation
6. Property management pages
7. Tenant management interface
8. Payment tracking dashboard
```

#### Phase 4: Tenant Portal
```
Create the tenant portal with:
1. Self-registration flow with Right to Rent verification
2. Document upload interface for required UK documents:
   - Passport/ID verification
   - Bank statements upload
   - Employment documentation
   - Reference requests
3. Payment management (direct debit setup, history)
4. Maintenance request system with photo uploads
5. Digital tenancy document access
6. Communication center with landlord
```

#### Phase 5: UK Compliance Features
```
Implement UK legal compliance:
1. Right to Rent document verification system
2. IDVT (Identity Document Validation Technology) integration
3. Safety certificate tracking (EPC, Gas Safety, EICR)
4. GDPR-compliant data handling
5. Deposit protection scheme integration
6. Anti-money laundering checks for high-value properties
```

#### Phase 6: Payment Integration
```
Implement automated payment system:
1. Open Banking API integration (TrueLayer or similar)
2. Stripe/GoCardless payment gateways
3. Automated payment matching to invoices
4. Direct debit mandate management
5. Payment reconciliation system
6. Late payment tracking and notifications
```

### Step 4: Using Cursor Effectively

#### Chat Commands to Use:
- **Cmd/Ctrl + L**: Open AI chat
- **Cmd/Ctrl + K**: Quick AI edit of selected code
- **Cmd/Ctrl + I**: AI code generation in current file

#### Best Practices:
1. **Be Specific**: Always mention "UK property management" and "PropertyFlow" in prompts
2. **Reference the Requirements**: Point Cursor to the `PropertyFlow_Requirements_Analysis.md` file
3. **Iterative Development**: Build one feature at a time, test, then move to next
4. **Use Context**: Select relevant files before asking Cursor to modify them

#### Sample Progressive Prompts:

**For Database Setup:**
```
Looking at the PropertyFlow requirements document, create the Drizzle schema for the properties table with UK-specific fields including postcode validation, property types (flat, house, terraced, etc.), and compliance certificate tracking.
```

**For Authentication:**
```
Create a role-based authentication system for PropertyFlow that handles both landlords and tenants with separate login flows and JWT token management.
```

**For UI Components:**
```
Create a property management dashboard for landlords using Shadcn/UI components that displays property portfolio, tenant status, payment tracking, and compliance alerts.
```

### Step 5: Development Workflow

1. **Start with Backend**: API routes and database schema
2. **Add Authentication**: User management and security
3. **Build Core Features**: Property and tenant management
4. **Add Compliance**: UK legal requirements
5. **Integrate Payments**: Open Banking and payment processing
6. **Polish UI/UX**: Mobile responsiveness and user experience
7. **Testing**: Comprehensive testing suite
8. **Deployment**: Production deployment setup

### Step 6: Key Files to Create First

Ask Cursor to create these files in order:
1. `package.json` (monorepo setup)
2. `apps/api/src/index.ts` (Express server)
3. `packages/database/schema.ts` (Drizzle schemas)
4. `apps/landlord-portal/src/main.tsx` (React app)
5. `apps/tenant-portal/src/main.tsx` (React app)
6. `packages/ui/components/` (Shared components)

### Step 7: Environment Setup

Create `.env` files for:
```
DATABASE_URL=postgresql://...
JWT_SECRET=...
STRIPE_SECRET_KEY=...
OPEN_BANKING_API_KEY=...
IDVT_API_KEY=...
```

### Pro Tips for Cursor:

1. **Use the Requirements Doc**: Always reference `PropertyFlow_Requirements_Analysis.md` in your prompts
2. **Build Incrementally**: Don't try to build everything at once
3. **Test Early**: Ask Cursor to create tests alongside features
4. **UK Focus**: Always mention UK compliance when building features
5. **Review Code**: Use Cursor's code review features to ensure quality

Start with Step 1 and work through each phase. Cursor will help you build a production-ready UK property management system following best practices!