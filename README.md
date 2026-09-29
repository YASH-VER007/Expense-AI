# ExpenseAI – AI-Powered Personal Expense Management System
> **"Track Smarter. Spend Better."**

Frontend architecture, design system, and foundational UI components built for Indian college students and young working professionals.

---

## 🚀 Tech Stack
- **Framework:** React 19 + Vite 8
- **Styling:** Tailwind CSS v4 (with `@theme` design tokens)
- **Icons:** Lucide React
- **Currency Engine:** Indian Rupees (`₹` / `INR`) strictly formatted with the Indian numbering system (`en-IN`)
- **Planned Analytics:** Recharts (ready for subsequent analytical pages)

---

## 📂 Project Structure
```text
expense-ai/
├── public/
├── src/
│   ├── assets/            # Static assets and graphics
│   ├── components/
│   │   ├── common/        # Atomic, reusable design system components
│   │   │   ├── AIInsightCard.jsx  # AI recommendation card with ₹ potential savings
│   │   │   ├── Alert.jsx          # Info, warning, success, danger & AI alerts
│   │   │   ├── Avatar.jsx         # User avatar initials with active status dot
│   │   │   ├── Badge.jsx          # Semantic status and AI badges
│   │   │   ├── Button.jsx         # Primary navy, secondary, AI purple, savings green
│   │   │   ├── Card.jsx           # Compound card layout (Header, Title, Content, Footer)
│   │   │   ├── CurrencyInput.jsx  # Fixed ₹ prefix, verbal Lakh/Thousand translation & presets
│   │   │   ├── Input.jsx          # Accessible inputs with prefix/suffix icons & errors
│   │   │   ├── Logo.jsx           # ExpenseAI text & wallet/sparkle icon
│   │   │   ├── Modal.jsx          # Keyboard accessible dialog with backdrop blur
│   │   │   ├── Select.jsx         # Styled dropdown selector with chevron
│   │   │   ├── StatCard.jsx       # FinTech metric display card with ₹ formatting & trends
│   │   │   └── index.js
│   │   └── layout/        # Shell layout components
│   │       ├── Container.jsx      # Responsive max-width wrappers
│   │       ├── Navbar.jsx         # Top navigation bar with INR indicator & persona switcher
│   │       ├── PageHeader.jsx     # Consistent view headers with action buttons
│   │       └── index.js
│   ├── data/
│   │   ├── mockData.js    # Realistic Indian student & young professional finances
│   │   └── navigation.js  # App navigation links and user menu definitions
│   ├── pages/
│   │   ├── DesignSystemPage.jsx  # Interactive showcase demonstrating all design tokens & UI components
│   │   └── index.js
│   ├── services/
│   │   ├── storageService.js     # User preferences & localStorage persistence
│   │   └── index.js
│   ├── utils/
│   │   ├── cn.js          # Safe Tailwind class merging (clsx + tailwind-merge)
│   │   ├── constants.js   # Indian expense categories, app config & personas
│   │   └── currency.js    # Indian numbering format (Lakhs, Crores, ₹ symbols)
│   ├── App.jsx            # Root application orchestrator
│   ├── index.css          # Tailwind CSS v4 design tokens and theme variables
│   └── main.jsx           # React DOM root entry
├── index.html             # Google Fonts (Plus Jakarta Sans & Inter) + Meta tags
├── package.json
└── vite.config.js         # Vite configuration with React and Tailwind plugins
```

---

## 🎨 Visual Style & Design Tokens

| Token | Hex | Usage |
|---|---|---|
| **Primary Navy** | `#0F1B2E` / `#1E3256` | Primary action buttons, brand logo, strong headings |
| **AI Purple Accent** | `#7C3AED` / `#8B5CF6` | AI smart tips, automated insights, AI badges |
| **Savings Green** | `#16A34A` / `#22C55E` | Positive cashflow, savings goals, surplus indicators |
| **Warning Amber** | `#F59E0B` | Budget threshold warnings, approaching spending limits |
| **Danger Red** | `#EF4444` | Deficit warnings, delete actions, validation errors |
| **Light Canvas** | `#F8FAFC` | Clean, glare-free background with soft card borders |

---

## 🇮🇳 Indian Rupee (₹ / INR) Currency Features
- **Strictly ₹ / INR**: No dollars ($), USD, euros (€), or pounds (£).
- **Indian Numbering Format**: Automatically formats `1,25,000` (1 Lakh 25 Thousand) and `1,50,00,000` (1.5 Crore) with `formatINR`.
- **Verbal Unit Preview**: As the user types into `CurrencyInput`, it translates amounts into Indian words (e.g. `₹45,000` $\rightarrow$ `≈ ₹45 Thousand`).
- **Quick Tap Presets**: One-tap `+₹100`, `+₹500`, `+₹1,000`, `+₹5,000` buttons for effortless mobile/desktop logging.

---

## 👥 Dual Target User Personas Built-In
1. **College Student (Aarav Mehta)**
   - Monthly Allowance: ₹15,000
   - Context: Canteen food, Chai Point, Metro smart card, semester books, hostel fees.
2. **Young Working Professional (Priya Sharma)**
   - Monthly Salary: ₹75,000
   - Context: Apartment rent, Nifty 50 SIPs, Blinkit groceries, weekend dining, electricity & broadband bills.

---

## 💻 Running the Application

1. Make sure you are in the project directory:
   ```powershell
   cd "C:\Users\jayve\.gemini\antigravity\scratch\expense-ai"
   ```

2. Run the development server:
   ```bash
   npm run dev
   ```

3. Open your browser at:
   ```text
   http://localhost:5173
   ```

4. Build for production:
   ```bash
   npm run build
   ```
