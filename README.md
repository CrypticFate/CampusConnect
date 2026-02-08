# CampusConnect

A student-driven marketplace platform built for campus communities. CampusConnect enables verified university students to buy, sell, and exchange items and services with their peers while maintaining safety, trust, and community integrity.

## Features

- **Verified Student Marketplace** – Browse, create, and manage product listings exclusively among verified university students.
- **Service Exchange Hub** – Offer and request services such as tutoring, design work, and more.
- **AI Price Advisor** – Get intelligent pricing suggestions powered by Google Gemini AI based on market data and item condition.
- **Bidding & Negotiation** – Place bids on listings, accept or reject offers, and send counter-offers with real-time status tracking.
- **Real-Time Messaging** – Communicate directly with buyers and sellers through Firebase-powered chat.
- **Notifications** – Stay informed with real-time notifications for bids, orders, messages, and moderation actions.
- **Shopping Cart & Checkout** – Add items to a cart and complete purchases through Stripe-powered checkout.
- **Order Management** – Track incoming and outgoing orders from purchase to completion.
- **Visibility Controls** – Limit listing visibility to your own university or open it to all participating institutions.
- **Safe Campus Meetups** – Organize secure meetups with interactive maps powered by Leaflet.
- **Admin & Moderation Dashboard** – Student-driven moderation with listing approval/rejection, user reporting, suspension management, and platform analytics.
- **User Profiles & Settings** – Manage your profile, view ratings and reviews, and configure account preferences.

## Tech Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React 18, TypeScript, Vite |
| **UI** | Tailwind CSS, shadcn/ui (Radix UI), Framer Motion |
| **Routing** | React Router v6 |
| **State & Data** | React Query, React Context |
| **Forms** | React Hook Form, Zod |
| **Backend & Database** | Firebase (Authentication, Firestore, Cloud Storage) |
| **Payments** | Stripe |
| **AI** | Google Generative AI (Gemini) |
| **Maps** | Leaflet, React-Leaflet |
| **Media** | Cloudinary |

## Project Structure

```
├── api/                        # Serverless API functions (Stripe checkout)
├── public/                     # Static assets
├── scripts/                    # Utility scripts
├── src/
│   ├── components/
│   │   ├── admin/              # Admin dashboard components
│   │   ├── layout/             # Shared layout (Navbar, etc.)
│   │   ├── marketplace/        # Marketplace feature components
│   │   └── ui/                 # shadcn/ui component library
│   ├── context/                # React context providers (Cart, Listings)
│   ├── hooks/                  # Custom React hooks
│   ├── lib/                    # Firebase config, Gemini AI, Stripe, caching, utilities
│   ├── pages/                  # Page-level route components
│   ├── services/               # Background services (cache warming)
│   ├── types/                  # TypeScript type definitions
│   ├── utils/                  # Utility functions
│   ├── App.tsx                 # Root component with route definitions
│   └── main.tsx                # Application entry point
├── index.html                  # HTML entry point
├── vite.config.ts              # Vite configuration
├── tailwind.config.ts          # Tailwind CSS configuration
└── tsconfig.json               # TypeScript configuration
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later recommended)
- npm (included with Node.js) – you can also install Node.js with [nvm](https://github.com/nvm-sh/nvm#installing-and-updating)

### Installation

```bash
# Clone the repository
git clone https://github.com/CrypticFate/CampusConnect.git

# Navigate to the project directory
cd CampusConnect

# Install dependencies
npm install

# Start the development server
npm run dev
```

The app will be available at **http://localhost:8080**.

### Environment Variables

Create a `.env` file in the project root with the following variables:

```env
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
VITE_GEMINI_API_KEY=your_gemini_api_key
```

### Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the development server on port 8080 |
| `npm run build` | Build the application for production |
| `npm run build:dev` | Build with development mode settings |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint to check for code issues |

## Contributing

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

