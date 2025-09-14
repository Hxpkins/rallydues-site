# RallyDues

A modern dues management platform for fraternities, sororities, and membership organizations.

## Features

- **Automated Dues Collection**: Set up dues cycles with automatic invoicing and payment reminders
- **Quick Pay**: Login-free payment system for members and parents using PayCodes
- **Member Management**: Import CSV rosters, generate PayCodes, and track member status
- **Payment Plans**: Flexible installment plans with treasurer approval
- **Multi-tenant Architecture**: Complete data isolation between organizations
- **Secure Processing**: Bank-level security with Stripe Connect integration

## Tech Stack

- **Framework**: Next.js 15 with App Router
- **Database**: Supabase (PostgreSQL)
- **Payments**: Stripe Connect
- **Email**: Resend
- **Styling**: Tailwind CSS with shadcn/ui components
- **Authentication**: Supabase Auth

## Quick Start

1. **Clone and Install**
   \`\`\`bash
   # Install dependencies (handled automatically in v0)
   npm install
   \`\`\`

2. **Environment Setup**
   - See [docs/SETUP.md](docs/SETUP.md) for detailed configuration instructions
   - Add required environment variables in v0 Project Settings

3. **Database Setup**
   - Run migration scripts in the `scripts/` folder
   - Scripts are executed automatically in v0

4. **Development**
   \`\`\`bash
   npm run dev
   \`\`\`

## Environment Variables

Key environment variables needed:

\`\`\`env
# Database
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key

# Email
RESEND_API_KEY=your_resend_api_key
SUPPORT_EMAIL=support@rallydues.com
EMAIL_FROM=RallyDues <support@rallydues.com>

# Payments
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_webhook_secret
NEXT_PUBLIC_SITE_URL=https://rallydues.com
\`\`\`

See [docs/SETUP.md](docs/SETUP.md) for complete setup instructions.

## Key Features

### For Treasurers
- Create and manage dues cycles
- Import member rosters via CSV
- Generate unique PayCodes for each member
- Track payments and outstanding balances
- Approve payment plan requests
- View financial analytics and reports

### For Members
- Pay dues without creating an account (Quick Pay)
- Request installment payment plans
- View payment history
- Receive automated reminders

### For Parents/Guests
- Pay member dues using PayCode + last name
- Choose between card and ACH payments
- Transparent fee disclosure
- Instant email confirmations

## Architecture

RallyDues is built with a multi-tenant architecture:

- **Organizations**: Each fraternity/sorority/group is a separate tenant
- **Users**: Members belong to organizations with role-based permissions
- **Dues Cycles**: Time-based collection periods with configurable amounts
- **Payments**: Processed via Stripe with fees distributed appropriately

## Payment Processing

- **Cards**: 3.1% processing surcharge (includes Apple Pay/Google Pay)
- **ACH/Bank Transfer**: No processing surcharge
- **Security**: PCI-compliant processing via Stripe
- **Multi-tenant**: Funds go directly to organization accounts

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

Copyright © 2025 RallyDues. All rights reserved.

## Support

- **Documentation**: [docs/SETUP.md](docs/SETUP.md)
- **Issues**: Contact support for technical issues
- **Email**: support@rallydues.com

---

Built with ❤️ for Greek life organizations and membership groups.
