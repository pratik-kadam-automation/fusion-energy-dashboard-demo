# Energy Monitoring Dashboard: Demo

I made this demo for the Fusion Electrotech energy monitoring upgrade, to show how the improved dashboard would look and work before anything gets built for real.

It runs on sample data only. It isn't connected to any meter, gateway or spreadsheet, and nothing you change in it is saved.

## Why I built it

I went through the current dashboard screen by screen. It works, but a few things make it hard to rely on:

- It doesn't show how old the data is, so stale readings look current.
- A meter that stops reporting shows as zero, which looks the same as a machine that is switched off.
- Alerts fire on tiny changes, so the real problems get buried.
- All 25 meters are shown as equal cards, even the idle ones.

This demo is my answer to each of those.

## What's in it

- **Dashboard:** a data-freshness bar, key figures, a short "needs attention" list, top 10 consumers, and a meter table you can search and sort. Click any row for a 30-day view.
- **Live Data:** latest reading for every meter, with search and filters.
- **Alerts:** only changes above a size you set, with a separate tab for insights like top usage and trends.
- **Reports:** period presets, a chart for the meters you pick, a daily table, and CSV or PDF export.
- **Admin:** hidden passwords, a minimum length, and a confirmation before removing a user.

The **Preview control** in the bottom right corner lets you see how the freshness bar changes when the data is 2 or 7 days old.

## Running it

Open `index.html` in a browser. There's nothing to install or build. To share it, put the folder on any static host such as Netlify or Cloudflare Pages.

## Things to know

- Costs are estimates at a rate per kWh you can edit. They aren't billing figures.
- In the demo, a spike is anything above 1.5 times the 13-day average, and a drop is anything below 0.4 times. Each also has to be bigger than the minimum size you set.
- It's a single HTML file with no external data requests.

Pratik Kadam, in cooperation with Infinity Automation
