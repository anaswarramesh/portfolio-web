# Personal Engineering Laboratory Portfolio

A modular, high-performance personal engineering portfolio built using vanilla HTML, CSS, and JavaScript. Designed for static hosting on GitHub Pages with zero build steps, node packages, or framework dependencies.

All dynamic content (projects, workbench updates, timeline build logs, and roadmap ideas) is driven by structured JSON datasets, making content updates simple and maintainable.

---

## Directory Structure

```text
my-engineering-lab/
├── index.html          # Main application layout and structure
├── style.css           # Engineering design system, theme variables, and animations
├── script.js           # Modular JS for fetching JSON datasets and handling filters
├── projects.json       # Project list, active workbench status, and tags
├── timeline.json       # Engineering build log entries
├── ideas.json          # Planned, active, and completed roadmap ideas
├── README.md           # Documentation and maintenance guide
└── assets/
    ├── images/         # Project screenshots and diagrams
    └── icons/          # Custom icons or media assets

1. Adding or Editing Projects (projects.json)
To add a new project, open projects.json and append a new JSON object inside the main array:

{
  "id": "proj-06",
  "title": "PROJ-06: Custom PCB USB Power Controller",
  "description": "Hardware project designing a USB-C Power Delivery negotiator.",
  "tags": ["Hardware", "Electronics"],
  "image": "assets/images/usb-pd.png",
  "github": "[https://github.com/yourusername/project-repo](https://github.com/yourusername/project-repo)",
  "demo": "[https://github.com/yourusername/project-repo](https://github.com/yourusername/project-repo)",
  "activeBuild": false
}

Tags: Using tags like "Hardware", "Software", "AI", "Raspberry Pi", "Android", "Electronics", "FPGA", "Research", or "Web Development" automatically connects the project to the category filter buttons on the site.

Images: Place project image files into assets/images/ and reference the relative path in the "image" field.

2. Updating the Current Workbench Build (projects.json)
To change which project appears in the "Current Active Build / Workbench" section:

Locate the project inside projects.json that you are currently working on.

Set "activeBuild": true.

Ensure all other projects have "activeBuild": false.

Include the "currentBuildDetails" object:

"activeBuild": true,
"currentBuildDetails": {
  "progress": 70,
  "completedTasks": [
    "Task 1 completed",
    "Task 2 completed"
  ],
  "upcomingTasks": [
    "Upcoming milestone 1",
    "Upcoming milestone 2"
  ],
  "estimatedCompletion": "Q4 2026"
}

3. Adding Entries to the Build Log (timeline.json)
The "Engineering Build Log" displays updates in a vertical timeline. Open timeline.json and add a new entry to the array. Place newer entries at the top so they display first:
[
  {
    "date": "AUGUST 2026",
    "title": "Hardware Rev 2.0 Assembly",
    "description": "Assembled the second board revision, verified voltage rails, and flashed updated firmware."
  }
]

4. Updating the Ideas & Research Roadmap (ideas.json)
Open ideas.json to organize project concepts across three columns (planned, inProgress, and completed):

{
  "planned": [
    {
      "title": "USB Oscilloscope",
      "description": "High-speed ADC streamer over USB CDC."
    }
  ],
  "inProgress": [],
  "completed": []
}

5. Updating Personal Bio, Links, and Resume (index.html)
To edit fixed content such as social links, email address, bio text, or resume links:

1.Open index.html.

2.Locate the relevant section (#about, #contact, or #github).

3.Update the text or href attributes directly in the HTML markup.

4.Save and commit your changes.

Technical Specifications
Language Standard: HTML5, CSS3, Vanilla JavaScript (ES6+)

External Dependencies: FontAwesome CDN (for standard UI icons)

Compatibility: All modern standard browsers (Chrome, Firefox, Safari, Edge)

Build Tools Required: None
