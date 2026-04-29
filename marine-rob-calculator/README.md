# Marine ROB Calculator 🚢

A professional fuel consumption & oil tracking app built for seafarers.

## Features

✅ **Fuel ROB Tracking** - Track HFO, VLSFO, MDO, Lube Oils, and Sludge separately
✅ **Consumption Logging** - Log daily fuel consumption with previous/current ROB
✅ **Bunker Management** - Record bunkering events with port, quantity, density
✅ **Contract Tracking** - Visual progress ring showing time remaining on contract
✅ **Salary Calculator** - Calculate daily rate and earnings during contract
✅ **Fuel Endurance** - Estimate days of fuel remaining
✅ **Multi-language** - English, Filipino, Russian, Ukrainian, Hindi
✅ **Theme Support** - Dark, Light, System modes
✅ **Local Storage** - All data stays on device, no cloud sync
✅ **PWA Ready** - Install as app on mobile
✅ **Contact** - Built-in email (nordaneastow@gmail.com)

## Tech Stack

- **React 19** + Vite
- **TypeScript** - Type-safe codebase
- **Tailwind CSS** - Responsive design
- **Lucide Icons** - Beautiful UI icons
- **localStorage** - Device-only data persistence

## Quick Start

### Prerequisites
- Node.js 16+
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/yourusername/marine-rob-calculator.git
cd marine-rob-calculator

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit `http://localhost:5173` in your browser.

### Build for Production

```bash
npm run build
```

Output will be in `dist/` directory.

## Project Structure

```
marine-rob-calculator/
├── src/
│   ├── App.tsx                 # Main app component
│   ├── main.tsx                # React entry point
│   ├── index.css               # Global styles + theme variables
│   ├── types.ts                # TypeScript interfaces
│   ├── i18n.ts                 # Translations (5 languages)
│   ├── localStore.ts           # localStorage wrapper
│   ├── theme.ts                # Theme management
│   ├── utils.ts                # Utility functions
│   ├── hooks/
│   │   └── useStore.ts         # React state management
│   └── components/
│       ├── SummaryTab.tsx       # Overview & fuel endurance
│       ├── FuelTab.tsx          # Tank management
│       ├── ConsumptionTab.tsx   # Daily consumption logging
│       ├── BunkerTab.tsx        # Bunker entry logging
│       ├── ContractTab.tsx      # Contract progress tracker
│       ├── SalaryTab.tsx        # Salary calculator
│       ├── SettingsScreen.tsx   # Theme, language, purchase
│       ├── CircularProgress.tsx # Progress ring component
│       ├── AdBanner.tsx         # Ad banner footer
│       ├── TankCard.tsx         # Tank display card
│       └── AddTankModal.tsx     # Add tank dialog
├── backend/
│   └── index.ts                # (Optional) Backend skeleton
├── public/
│   ├── icon.svg                # App icon
│   ├── icon-192.svg            # PWA icon
│   └── manifest.json           # PWA manifest
├── tests/
│   └── tests.txt               # E2E test specs
├── index.html                  # HTML entry
├── vite.config.ts              # Vite configuration
├── tailwind.config.js          # Tailwind theming
├── postcss.config.js           # PostCSS config
├── tsconfig.json               # TypeScript config
└── package.json                # Dependencies
```

## Data Storage

All data is stored in **browser localStorage** under these keys:
- `mrob_tanks` - Tank records
- `mrob_bunker` - Bunker log
- `mrob_consumption` - Consumption records
- `mrob_contract` - Active contract
- `mrob_contract_history` - Finished contracts
- `mrob_salary` - Salary data
- `mrob_ad_free` - Ad-free purchase status
- `mrob_theme` - Theme preference
- `mrob_locale` - Language selection

**No data leaves your device.**

## Features by Tab

### Overview
- Total ROB summary by fuel type
- Fuel endurance calculator (days remaining)
- Share app button
- Visual bar charts

### Tanks
- Add/edit/delete fuel tanks per category
- Track volume (m³), density (t/m³)
- Auto-calculate mass (MT)
- Supports: HFO, VLSFO, MDO, Lube Oils, Sludge

### Log
- **Consumption**: Log daily consumption (previous ROB → current ROB)
- **Bunker**: Record bunkering events with port, quantity, density
- Edit or delete past entries

### Crew
- **Contract**: Track contract progress with visual ring
  - Vessel name, rank, total days, sign-on date
  - Displays days remaining + motivational messages
  - Finish & archive contracts
  
- **Salary**: Calculate earnings
  - Monthly salary, currency selection
  - Daily rate calculation
  - Earned vs. remaining

### Settings
- **Theme**: Dark, Light, System
- **Language**: EN, Filipino, Russian, Ukrainian, Hindi
- **Remove Ads**: $4.99 one-time purchase
- **Contact**: Email link for feedback
- **About**: Version and data privacy info

## Deployment

### Deploy to AppDeploy (Recommended)
1. Create account at [appdeploy.ai](https://appdeploy.ai)
2. Connect your GitHub repository
3. Select "React + Vite" template
4. Deploy with one click
5. Get instant public URL

### Deploy to Vercel
```bash
npm install -g vercel
vercel
```

### Deploy to Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod --dir=dist
```

## Customization

### Change App Name
Edit in multiple places:
- `src/i18n.ts` - `appName`
- `index.html` - `<title>`
- `public/manifest.json` - `"name"`
- `package.json` - `"name"`

### Change Contact Email
Edit in `src/i18n.ts` and components:
- Search for `nordaneastow@gmail.com`
- Replace with your email

### Add More Languages
1. Edit `src/i18n.ts`
2. Add new `Locale` type
3. Add translations object
4. Add to language selector in `SettingsScreen.tsx`

### Customize Colors
Edit `src/types.ts`:
```typescript
export const FUEL_COLORS: Record<FuelCategory, string> = {
  HFO: 'bg-orange-600',     // Change these
  VLSFO: 'bg-amber-500',
  // etc...
};
```

## Troubleshooting

**Data lost after refresh?**
→ Check if cookies/storage are blocked. Try incognito mode.

**App not loading?**
→ Clear browser cache. Check console (F12) for errors.

**Numbers showing wrong?**
→ Ensure density values are in t/m³ (typically 0.85-1.0 for oils)

## Contributing

Found a bug or have a feature idea?
→ Email: **nordaneastow@gmail.com**

## License

MIT License - Free to use, modify, and distribute.

## Credits

Built with ❤️ for seafarers by developers who understand maritime operations.

---

**Version:** 2.0.0  
**Last Updated:** April 2026  
**Status:** Production Ready ✅
