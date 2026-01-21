# Xrota

A staff scheduling application with automatic rota generation using a fair 5-week rotation system.

**Live Demo:** [rota-pants.vercel.app](https://rota-pants.vercel.app)

## Features

- **5-week rotating schedule** with predictable, consistent shifts
- **Fair weekend distribution** - exactly 2 weekends per person over 5 weeks
- **Consistent shift blocks** - staff work the same shift type all week (no daily changes)
- **Consecutive days off** - no split days off
- **Auto-generation** - generate single weeks or complete 5-week cycles
- **Hourly coverage graph** - visual display of staffing levels
- **Shift distribution stats** - track shift fairness over time
- **Dark mode** support
- **Print/export** - print single weeks or multi-week ranges with summary
- **CSV import/export** - backup and restore schedules
- **LocalStorage persistence** - data saved in browser

## How It Works

### The 5-Week Cycle

Each week, staff are divided into two groups:

| Weekend Workers (2 people) | Weekday-Only Workers (3 people) |
|---------------------------|--------------------------------|
| Work Saturday and Sunday | Work Monday to Friday only |
| Get 2 consecutive weekdays off | Have Saturday and Sunday off |
| Work Floating shifts on weekdays | Work the same shift type all 5 weekdays |

### Shift Types

| Shift | Hours | Time | Purpose |
|-------|-------|------|---------|
| **Early** | 7.5 hrs | 08:00 - 16:30 | Opens the business |
| **Mid** | 7.5 hrs | 10:00 - 18:30 | Covers midday peak |
| **Late** | 7.5 hrs | 12:00 - 20:30 | Closes the business |
| **Floating** | 7.5 hrs | 08:30 - 17:00 | Flexible coverage |

### Weekly Guarantees

For each staff member, every week:
- Exactly **37.5 working hours** (5 shifts x 7.5 hours)
- Exactly **2 consecutive days off**
- **12 hours minimum rest** between shifts

### 5-Week Totals (identical for all staff)

- Early: 7 shifts
- Mid: 5 shifts
- Late: 7 shifts
- Floating: 6 shifts
- **Total: 25 shifts = 187.5 hours**

## Usage

1. Click **"Generate 5 Weeks"** to create a complete rotation cycle
2. Use **Prev/Next** buttons to navigate between weeks
3. Click a shift button, then click a cell to manually edit
4. Use **"Print Schedule"** to print single or multiple weeks
5. **"Import/Export CSV"** to backup or restore data

## Documentation

See [docs/algorithm-guide.html](docs/algorithm-guide.html) for a detailed guide suitable for HR and management.

## Tech Stack

- Vanilla HTML/CSS/JavaScript
- No build process required
- LocalStorage for data persistence
- Deployed on Vercel

## License

MIT
