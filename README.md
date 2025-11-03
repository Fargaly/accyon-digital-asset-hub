# ACCYON - Digital Asset Hub Platform

## Overview
ACCYON is a controlled marketplace Digital Asset Hub (DAH) platform facilitating multi-sided B2B value creation. It connects interior designers/consultants with manufacturers, enabling BIM/CAD plugin integration for project creation and asset submission.

## Recent Sprint Progress (November 2025)

### ✅ Sprint 8A: Security & Infrastructure (Complete)
- Four-tier rate limiting (Public, Authenticated, Admin, Plugin)
- Comprehensive audit logging for critical operations
- Domain-based security with host-header spoofing prevention
- Multi-domain architecture (accyon.net + accyon.xyz for admin)

### ✅ Visual Hierarchy Enhancement (Complete)
- Implemented shade varieties of golden accent color
- Vibrant gold (HSL 43 95% 50%) for primary CTAs
- Softer cream/brown tones for navigation states
- Improved visual distinction across UI components

### ✅ Sprint 9: Profile Settings (Complete)
- Full profile management interface
- Avatar upload with object storage integration
- Bio, company, phone fields with validation
- Account details display (role badge, member since)
- React Hook Form + Zod validation

### ✅ Sprint 10: Developer Role (Complete)
- New "developer" role added to RBAC system
- API-focused permissions (API key management)
- Dedicated navigation (Catalog + API Keys)
- Full API key lifecycle management (CRUD)
- Proper role-based redirects

### 🔄 Sprint 12: Multi-Format Downloads (API Complete)
**Implemented:**
- Format parameter support (GLB, FBX, OBJ, USDZ)
- Format validation and metadata responses
- Backward-compatible API design
- Clear communication of current capabilities

**Pending:**
- Format conversion service (requires external tools)
- Conversion job queue and caching
- Tools needed: gltf-pipeline, obj2gltf, usd_from_gltf

## Tech Stack

### Frontend
- React 18, TypeScript
- Wouter (routing), TanStack Query v5 (state)
- Shadcn UI + Radix UI components
- Tailwind CSS with custom design system
- React Hook Form + Zod validation

### Backend
- Node.js + Express
- PostgreSQL + Drizzle ORM
- Firebase Auth (email, phone, Google, GitHub)
- Dual API architecture (/v1/* web, /plugin/v1/* plugins)
- Replit Object Storage (presigned URLs)

### Security
- Role-Based Access Control (Designer, Manufacturer, Admin, Developer)
- Four-tier rate limiting
- Audit logging for critical operations
- Domain-based admin access control
- JWT + API key authentication

## Key Features

### For Manufacturers
- Asset upload with 3D model support (GLB/GLTF)
- Metadata management (category, material, dimensions, pricing)
- Controlled approval workflow (draft → pending → approved/rejected)
- Multi-currency pricing with discounts

### For Designers
- Project management and organization
- Quotation generation with inline editing
- Shopping cart functionality
- BIM/CAD plugin integration via API keys
- Download history and KPIs

### For Admins
- User management and role assignment
- Asset moderation queue
- Invite code system for controlled access
- Platform statistics and analytics
- Domain-restricted admin panel (accyon.xyz)

### For Developers
- API key management for integrations
- Plugin testing capabilities
- Asset catalog access (read-only)
- Simplified API-focused interface

## Architecture Highlights

- **Universal Profile Merging:** Automatic profile consolidation across auth providers
- **Object Storage:** Presigned URLs for secure asset/avatar uploads
- **Multi-Domain Security:** Separate domains for platform and admin access
- **Audit Trail:** Comprehensive logging of all critical operations
- **Rate Limiting:** Tiered approach (200-1000 req/15min based on role)

## Development

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Database operations
npm run db:push      # Sync schema
npm run db:studio    # Open Drizzle Studio
```

## Documentation
- Technical docs: `replit.md`
- Security audit: `SECURITY_AUDIT.md`
- Design guidelines: Custom Shadcn theme with golden accents

---

**Status:** Active Development | **Last Updated:** November 2025
