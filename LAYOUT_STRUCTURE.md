# Gas Detector Dashboard - Layout Structure

## Main Application Structure

```
┌─────────────────────────────────────────────────────────────────┐
│                        HEADER SECTION                           │
├─────────────────────────────────────────────────────────────────┤
│  🏠 Gas Leak Monitoring Dashboard    [⚙️ System Setup]        │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                      DASHBOARD TABS                             │
├─────────────────────────────────────────────────────────────────┤
│  [📊 Real-time Readings] [🏢 Floor Plan] [📈 Analysis]         │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                    TAB CONTENT AREA                             │
└─────────────────────────────────────────────────────────────────┘
```

## Tab 1: Real-time Readings Layout

```
┌─────────────────────────────────────────────────────────────────┐
│                    READINGS HEADER                              │
├─────────────────────────────────────────────────────────────────┤
│  Real-time Gas Sensor Readings                                  │
│  🟢 System Online    Last Update: 12:34:56                     │
│  [🧪 Start Data Simulation] [⏹️ Stop Simulation]              │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                    SENSOR CONTAINER                             │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                ESP Module 1                             │   │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐       │   │
│  │  │ ESP1_Sensor1│ │ ESP1_Sensor2│ │ ESP1_Sensor3│       │   │
│  │  │ 234 ppm     │ │ 1567 ppm    │ │ 89 ppm      │       │   │
│  │  │ 🟢 NORMAL   │ │ 🟡 WARNING  │ │ 🟢 NORMAL   │       │   │
│  │  └─────────────┘ └─────────────┘ └─────────────┘       │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                ESP Module 2                             │   │
│  │  ┌─────────────┐ ┌─────────────┐                       │   │
│  │  │ ESP2_Sensor1│ │ ESP2_Sensor2│                       │   │
│  │  │ 1456 ppm    │ │ 234 ppm     │                       │   │
│  │  │ 🔴 HIGH ALERT│ │ 🟢 NORMAL   │                       │   │
│  │  └─────────────┘ └─────────────┘                       │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
```

## Tab 2: Floor Plan Layout

```
┌─────────────────────────────────────────────────────────────────┐
│                    FLOOR PLAN HEADER                            │
├─────────────────────────────────────────────────────────────────┤
│  Floor Plan & Sensor Locations                                  │
│  🟢 All sensors normal (4 sensors)                             │
│  [Reset View]                                                   │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                    FLOOR PLAN CONTAINER                         │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                FLOOR PLAN CANVAS                        │   │
│  │                                                         │   │
│  │    ┌─────────────────────────────────────────────┐     │   │
│  │    │                                             │     │   │
│  │    │  🏢 Facility Floor Plan                     │     │   │
│  │    │                                             │     │   │
│  │    │     🔴[1]     🟡[2]                        │     │   │
│  │    │                                             │     │   │
│  │    │        🟢[3]     🟢[4]                     │     │   │
│  │    │                                             │     │   │
│  │    │  🔴 = Critical (>1300 ppm)                  │     │   │
│  │    │  🟡 = Warning (>1000 ppm)                   │     │   │
│  │    │  🟢 = Normal (<1000 ppm)                    │     │   │
│  │    └─────────────────────────────────────────────┘     │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                SENSOR LEGEND                            │   │
│  ├─────────────────────────────────────────────────────────┤   │
│  │  🔴 ESP1_Sensor1    ESP 1 - Sensor 1                   │   │
│  │  🟡 ESP1_Sensor2    ESP 1 - Sensor 2                   │   │
│  │  🟢 ESP2_Sensor1    ESP 2 - Sensor 1                   │   │
│  │  🟢 ESP2_Sensor2    ESP 2 - Sensor 2                   │   │
│  │                                                         │   │
│  │  Alert Levels:                                          │   │
│  │  🔴 Critical: >1300 ppm                                │   │
│  │  🟡 Warning: >1000 ppm                                 │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
```

## Tab 3: Analysis Layout

```
┌─────────────────────────────────────────────────────────────────┐
│                    ANALYSIS HEADER                              │
├─────────────────────────────────────────────────────────────────┤
│  Gas Level Analysis & Trends    [Last 24 Hours ▼]              │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                    ANALYSIS CONTENT                             │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐   │
│  │ Current Status  │ │ Peak Readings   │ │ Alert History   │   │
│  │                 │ │                 │ │                 │   │
│  │ Normal: 2       │ │ ESP1_Sensor2    │ │ 12:34:56        │   │
│  │ Warning: 1      │ │ 1567 ppm        │ │ ESP1_Sensor2    │   │
│  │ Alert: 1        │ │ ESP2_Sensor1    │ │ WARNING         │   │
│  │                 │ │ 1456 ppm        │ │ 1567 ppm        │   │
│  └─────────────────┘ └─────────────────┘ └─────────────────┘   │
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                GAS LEVEL TRENDS                         │   │
│  │                                                         │   │
│  │  ┌─────────────────────────────────────────────────┐   │   │
│  │  │                                                 │   │   │
│  │  │  📈 Gas Level Trends Chart                      │   │   │
│  │  │                                                 │   │   │
│  │  │  ┌─┐                                           │   │   │
│  │  │  │ │     ┌─┐                                   │   │   │
│  │  │  │ │ ┌─┐ │ │ ┌─┐                               │   │   │
│  │  │  │ │ │ │ │ │ │ │                               │   │   │
│  │  │  └─┘ └─┘ └─┘ └─┘                               │   │   │
│  │  └─────────────────────────────────────────────────┘   │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
```

## Responsive Layout Behavior

### Desktop (>1024px)
- Side-by-side layout for floor plan and legend
- Full width sensor cards
- Horizontal analysis cards

### Tablet (768px - 1024px)
- Stacked floor plan layout
- Reduced legend width
- Responsive sensor cards

### Mobile (<768px)
- Vertical stacked layout
- Full width components
- Compact controls and buttons
- Scrollable legend

## Color Coding System

### Status Indicators
- 🟢 **Green**: Normal operation (<1000 ppm)
- 🟡 **Yellow**: Warning level (1000-1300 ppm)
- 🔴 **Red**: Critical level (>1300 ppm)
- ⚫ **Gray**: Disconnected/Error

### Floor Plan Highlighting
- **No Box**: Normal values
- **Yellow Box**: Warning values (>1000 ppm)
- **Red Box**: Critical values (>1300 ppm)

## File Structure
```
GasDetectorDashbord/
├── index.html              # Main dashboard
├── setup.html              # Setup page
├── script.js               # Dashboard JavaScript
├── setup.js                # Setup page JavaScript
├── style.css               # Main styles
├── setup.css               # Setup page styles
├── server.js               # Node.js backend
└── package.json            # Dependencies
```

